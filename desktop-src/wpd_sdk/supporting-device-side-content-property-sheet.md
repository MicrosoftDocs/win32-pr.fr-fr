---
title: Prise en charge du contenu côté appareil (feuille)
description: Prise en charge du contenu Device-Side
ms.assetid: ea11f8e6-fb53-46e4-b210-2dae33cdc056
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7e054e4c545acd8f34583da5cd9ef3af347643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319942"
---
# <a name="supporting-device-side-content"></a>Prise en charge du contenu côté appareil

Étant donné que le contenu côté appareil n’est pas accessible par le biais du système de fichiers dans Windows Vista, vous devez utiliser l’API shell Windows ou l’API WPD pour récupérer des données pour les objets périphérique. Il s’agit de la principale différence entre un gestionnaire de feuille de propriétés normal et un gestionnaire de feuille de propriétés WPD. L’exemple de code suivant illustre la récupération du contenu côté appareil à l’aide de l’API du shell Windows.

La première étape est l’initialisation de la liste d’identificateurs d’élément ou de PIDL. (Cette liste contient l’identificateur unique pour l’objet d’appareil donné.)


```C++
HRESULT CWPDPropSheet::_InitializePIDLArray(IDataObject *pDataObj)
{
    if (m_cfHIDA == 0)
    {
        m_cfHIDA = (CLIPFORMAT)RegisterClipboardFormat(CFSTR_SHELLIDLIST);
    }

    STGMEDIUM   medium;
    FORMATETC   fmte = {m_cfHIDA, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};

    m_pPropInfo = (PROPINFO*)LocalAlloc(LPTR, sizeof(PROPINFO));
    if (m_pPropInfo == NULL)
        return E_OUTOFMEMORY;

    AddRef_PropInfo(m_pPropInfo);

    HRESULT hr = pDataObj->GetData(&fmte, &medium);
    if (SUCCEEDED(hr))
    {
        SIZE_T cb = GlobalSize(medium.hGlobal);
        CIDA *pida = (CIDA*)GlobalAlloc(GPTR, cb);
        if (pida)
        {
            void *pv = GlobalLock(medium.hGlobal);
            if (pv != NULL)
            {
                CopyMemory(pida, pv, cb);
                GlobalUnlock(medium.hGlobal);
                m_pPropInfo->pida = pida;
                _ExaminePIDLArray();
            }
            else
            {
                hr = E_UNEXPECTED;
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
        ReleaseStgMedium(&medium);
    }

    return hr;
}
```



La fonction d’initialisation appelle la \_ fonction ExaminePIDLArray, qui récupère les propriétés de l’objet identifié par un PIDL dans le tableau PIDL.


```C++
HRESULT CWPDPropSheet::_ExaminePIDLArray()
{
    CComPtr<IShellFolder2> spParentFolder;

    CComVariant  variant;

    LPITEMIDLIST pidl = NULL;
    HRESULT      hr = S_OK;
    UINT         index = 0;

    pidl = GetPIDL(m_pPropInfo->pida, index);
    if (pidl)
    {
        hr = SHBindToParent(pidl, IID_PPV_ARGS(&spParentFolder), NULL);
        IF_FAILED_JUMP(hr, Exit);
    }

    do
    {
        CComPtr<IPropertySetStorage> spSetStorage;
        CComPtr<IPropertyStorage>    spPropStorage;

        // Get the IpropertySetStorage interface for this PIDL. This method could also
        // be used to retrieve an IPortableDevice interface to allow more low-level interaction
        // with the WPD API.
        hr = spParentFolder->BindToObject(ILFindLastID(pidl), NULL, IID_PPV_ARGS(&spSetStorage));
        if (SUCCEEDED(hr))
        {
            hr = spSetStorage->Open(WPD_FUNCTIONAL_OBJECT_PROPERTIES_V1, STGM_READ, &spPropStorage);
            if (SUCCEEDED(hr))
            {
                PROPVARIANT PropVar = {0};
                PROPSPEC    PropSpec = {0};

                PropSpec.ulKind = PRSPEC_PROPID;
                PropSpec.propid = 2; // WPD_FUNCTIONAL_OBJECT_CATEGORY

                PropVariantInit(&PropVar);

                hr = spPropStorage->ReadMultiple(1, &PropSpec, &PropVar);
                if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                {
                    // The PIDL array contains a non-file object.
                    // This means we don't want to take over the
                    // default menu action.
                    m_bPIDAContainsOnlyFiles = FALSE;
                    PropVariantClear(&PropVar);
                    break;
                }
                else
                {
                    CComPtr<IPropertyStorage>    spObjectProperties;
                    hr = spSetStorage->Open(WPD_OBJECT_PROPERTIES_V1, STGM_READ, &spObjectProperties);
                    if (SUCCEEDED(hr))
                    {
                        PropSpec.ulKind = PRSPEC_PROPID;
                        PropSpec.propid = 7; // WPD_OBJECT_CONTENT_TYPE
                        
                        PropVariantClear(&PropVar);
                        hr = spObjectProperties->ReadMultiple(1, &PropSpec, &PropVar);
                        if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                        {
                            if (IsEqualGUID(*PropVar.puuid, WPD_CONTENT_TYPE_FOLDER))
                            {
                                // The PIDL array contains a folder object.
                                // This means we don't want to take over the
                                // default menu action.
                                m_bPIDAContainsOnlyFiles = FALSE;
                                PropVariantClear(&PropVar);
                                break;
                            }
                        }
                    }
                }

                PropVariantClear(&PropVar);
            }
        }

        UI_SAFE_ILFREE(pidl);

        pidl = GetPIDL(m_pPropInfo->pida, ++index);
    } while (pidl != NULL && index < m_pPropInfo->pida->cidl);

Exit:
    UI_SAFE_ILFREE(pidl);
    return hr;
}
```



En plus de l’initialisation et du traitement de la liste d’identificateurs d’élément, votre application doit implémenter la méthode IShellPropSheetExt :: ReplacePage et insérer les gestionnaires de remplacement appropriés. Le shell Windows appelle cette méthode chaque fois qu’il est sur le point d’afficher une feuille de propriétés remplaçable, donnant à votre application la possibilité d’appeler un gestionnaire de remplacement correspondant. Le mot de poids faible du premier paramètre de la méthode ReplacePage est un identificateur pour la feuille de propriétés donnée que Windows va afficher. Les valeurs passées dans le mot de poids faible du premier paramètre correspondent aux valeurs définies dans le fichier WpdShellExtension. h. Ces valeurs et leurs descriptions apparaissent dans le tableau suivant.



| Valeur                                  | Description                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| WPDNSE \_ PROPSHEET \_ appareil \_ général     | Correspond à l’onglet général de l’appareil.                              |
| \_ \_ stockage général WPDNSE \_ PROPSHEET    | Correspond à l’onglet général pour un objet de stockage trouvé sur l’appareil.    |
| WPDNSE \_ PROPSHEET \_ contenu \_ général    | Correspond à l’onglet général pour l’objet de contenu trouvé sur l’appareil.      |
| \_références de \_ contenu WPDNSE PROPSHEET \_ | Correspond à l’onglet Références pour un objet de contenu trouvé sur l’appareil. |
| \_ressources de \_ contenu WPDNSE PROPSHEET \_  | Correspond à l’onglet ressources pour un objet de contenu trouvé sur l’appareil.  |
| \_Détails du \_ contenu WPDNSE PROPSHEET \_    | Correspond à un onglet Détails pour un objet de contenu trouvé sur l’appareil.      |



 

Dans l’exemple d’extension de la feuille de propriétés, la méthode ReplacePage appelle deux gestionnaires \_ de remplacement : ReplaceDeviceGeneral et \_ ReplaceContentReferences. Ces gestionnaires remplacent les onglets général du périphérique et références du contenu dans les feuilles de propriétés extensibles.


```C++
STDMETHODIMP CWPDPropSheet::ReplacePage(UINT uPageID, LPFNADDPROPSHEETPAGE lpfnReplacePage, LPARAM lParam)
{
    HRESULT       hr = S_OK;

    if (LOWORD(uPageID) == WPDNSE_PROPSHEET_DEVICE_GENERAL)
    {
        hr = _ReplaceDeviceGeneral(HIWORD(uPageID), lpfnReplacePage, lParam);
    }
    else if (LOWORD(uPageID) == WPDNSE_PROPSHEET_CONTENT_REFERENCES)
    {
        hr = _ReplaceContentReferences(HIWORD(uPageID), lpfnReplacePage, lParam);
    }

    return hr;
}
```



Étant donné qu’un utilisateur peut sélectionner plusieurs appareils, une application doit enregistrer le tableau PIDL retourné par IShellExtInit :: Initialize, puis examiner le mot haut du premier paramètre de ReplacePage. Une valeur de zéro dans ce mot haute correspond au premier élément dans le tableau PIDL, la valeur un correspond au deuxième élément, et ainsi de suite. Dans la fonction ReplacePage de l’exemple d’application, cette valeur de mot haute est passée aux deux gestionnaires de remplacement. Ces gestionnaires utilisent ensuite cette valeur pour identifier un appareil particulier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 



