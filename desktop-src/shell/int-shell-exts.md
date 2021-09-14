---
description: La majeure partie de l’implémentation d’un objet de gestionnaire d’extensions de Shell est dictée par son type. Toutefois, il existe des éléments communs. Cette rubrique décrit les aspects de l’implémentation qui sont partagés par tous les gestionnaires d’extensions de Shell.
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: Initialisation des gestionnaires d’extensions de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a27b6273c5e342dc4caf545fb3593cdad66261
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235229"
---
# <a name="initializing-shell-extension-handlers"></a>Initialisation des gestionnaires d’extensions de Shell

La majeure partie de l’implémentation d’un objet de gestionnaire d’extensions de Shell est dictée par son type. Toutefois, il existe des éléments communs. Cette rubrique décrit les aspects de l’implémentation qui sont partagés par tous les gestionnaires d’extensions de Shell.

Tous les gestionnaires d’extensions de Shell sont des objets COM (Component Object Model) in-process. Ils doivent recevoir un GUID et être inscrits comme décrit dans [inscription des gestionnaires d’extensions de Shell](handlers.md). Elles sont implémentées en tant que dll et doivent exporter les fonctions standard suivantes :

-   [**DllMain**](../dlls/dllmain.md). Point d’entrée standard de la DLL.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Expose la fabrique de classe de l’objet.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM appelle cette fonction pour déterminer si l’objet dessert des clients. Si ce n’est pas le cas, le système peut décharger la DLL et libérer la mémoire associée.

Comme tous les objets COM, les gestionnaires d’extensions de Shell doivent implémenter une interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) et une [fabrique de classe](../com/implementing-iclassfactory.md). la plupart d’entre eux doivent également implémenter une interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ou [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) dans Windows XP ou une version antérieure. celles-ci ont été remplacées par [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) et [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) dans Windows Vista. L’interpréteur de commandes utilise ces interfaces pour initialiser le gestionnaire.

L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) doit être implémentée par les éléments suivants :

-   Gestionnaires d’icônes
-   Gestionnaires de données
-   Gestionnaires de suppression

L’interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) doit être implémentée par les éléments suivants :

-   Gestionnaires de menus contextuels
-   Gestionnaires de glisser-déplacer
-   Gestionnaires de feuille de propriétés

Les sujets suivants sont abordés dans le reste de cette rubrique :

-   [Implémentation de IPersistFile](#implementing-ipersistfile)
-   [Implémentation de IShellExtInit](#implementing-ishellextinit)
-   [Personnalisation de l’info-bulle](#infotip-customization)
-   [Rubriques connexes](#related-topics)

## <a name="implementing-ipersistfile"></a>Implémentation de IPersistFile

L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) est conçue pour permettre le chargement d’un objet à partir de ou son enregistrement dans un fichier sur disque. Il a six méthodes en plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), cinq propres et la méthode [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) qu’il hérite de l’interface [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist). Avec les extensions de Shell, **IPersist** est utilisé uniquement pour initialiser un objet de gestionnaire d’extensions de Shell. Étant donné qu’il n’est généralement pas nécessaire de lire ou d’écrire sur le disque, seules les méthodes **GetClassID** et [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) requièrent une implémentation sans jeton.

L’interpréteur de commandes appelle d’abord [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) , et la fonction retourne l’identificateur de classe (CLSID) de l’objet de gestionnaire d’extensions. L’interpréteur de commandes appelle ensuite la [**charge**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) et passe deux valeurs. La première, *pszFile*, est une chaîne Unicode avec le nom du fichier ou du dossier sur lequel l’interpréteur de commandes va fonctionner. Le deuxième est *dwMode*, qui indique le mode d’accès au fichier. Étant donné qu’il n’est normalement pas nécessaire d’accéder aux fichiers, *dwMode* est généralement égal à zéro. La méthode stocke ces valeurs en fonction des besoins pour une référence ultérieure.

Le fragment de code suivant illustre la façon dont un gestionnaire d’extensions de Shell standard implémente les méthodes [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) et [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) . Il est conçu pour gérer ANSI ou Unicode. CLSID \_ SampleExtHandler est le GUID de l’objet de gestionnaire d’extensions et CSampleShellExtension est le nom de la classe utilisée pour implémenter l’interface. Les variables **m \_ szFileName** et **m \_ dwMode** sont des variables privées utilisées pour stocker le nom et les indicateurs d’accès du fichier.


```C++
class CSampleShellExtension : public IPersistFile
{
    // Method declarations not included

    private:
    WCHAR m_szFileName[MAX_PATH];    // The file name
    DWORD m_dwMode;                  // The file access mode
}

IFACEMETHODIMP CSampleShellExtension::GetClassID(__out CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

IFACEMETHODIMP CSampleShellExtension::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(m_szFileName, ARRAYSIZE(m_szFileName), pszFile); 
}

// The implementation sample is continued in the next section.
```



## <a name="implementing-ishellextinit"></a>Implémentation de IShellExtInit

L’interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) n’a qu’une seule méthode, [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), en plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). La méthode a trois paramètres que l’interpréteur de commandes peut utiliser pour passer divers types d’informations. Les valeurs transmises dépendent du type de gestionnaire, tandis que d’autres peuvent avoir la valeur **null**.

-   *pidlFolder* contient le pointeur d’un dossier vers une liste d’identificateurs d’éléments (PIDL). Il s’agit d’un PIDL absolu. Pour les extensions de feuille de propriétés, cette valeur est **null**. Pour les extensions de menu contextuel, il s’agit de l’PIDL du dossier qui contient l’élément dont le menu contextuel est affiché. Pour les gestionnaires de glisser-déplacer non par défaut, il s’agit de l’PIDL du dossier cible.
-   *pDataObject* contient un pointeur vers l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) d’un objet de données. L’objet de données contient un ou plusieurs noms de fichiers au format [CF \_ HDROP](dragdrop.md) .
-   *hRegKey* contient une clé de Registre pour l’objet de fichier ou le type de dossier.

La méthode [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) stocke le nom de fichier, le pointeur [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) et la clé de Registre nécessaires pour une utilisation ultérieure. Le fragment de code suivant illustre une implémentation de **IShellExtInit :: Initialize**. Pour plus de simplicité, cet exemple suppose que l’objet de données ne contient qu’un seul fichier. En général, l’objet de données peut contenir plusieurs fichiers, chacun d’entre eux devant être extrait.


```C++
// This code continues the CSampleShellExtension sample shown in the
// "Implementing IPersistFile" section above.

class CSampleShellExtension : public IShellExtInit
{
    // Method declarations not included
    
    private:
    // IDList of the folder for extensions invoked on the folder, such as 
    // background context menu handlers or nondefault drag-and-drop handlers. 
    PIDLIST_ABSOLUTE m_pidlFolder;
    
    // The data object contains an expression of the items that the handler is 
    // being initialized for. Use SHCreateShellItemArrayFromDataObject to 
    // convert this object to an array of items. Use SHGetItemFromObject if you
    // are only interested in a single Shell item. If you need a file system
    // path, use IShellItem::GetDisplayName(SIGDN_FILESYSPATH, ...).
    IDataObject *m_pdtobj;
    
    // For context menu handlers, the registry key provides access to verb 
    // instance data that might be stored there. This is a rare feature to use 
    // so most extensions do not need this variable.
    HKEY m_hRegKey;             
}
    
// This method must be very efficient. Do not do any unnecessary work here.
// Use Initialize to acquire resources that will be used later.

IFACEMETHODIMP CSampleShellExtension::Initialize(__in_opt PCIDLIST_ABSOLUTE pidlFolder,
                                                 __in_opt IDataObject *pDataObject, 
                                                 __in_opt HKEY hRegKey) 
{ 
    // In some cases, handlers are initialized multiple times. Therefore, 
    // clear any previous state here.
    CoTaskMemFree(m_pidlFolder);
    m_pidlFolder = NULL;
    
    if (m_pdtobj)
    { 
        m_pdtobj->Release(); 
    }
    
    if (m_hRegKey)
    {
        RegCloseKey(m_hRegKey);
        m_hRegKey = NULL;
    }
    
    // Capture the inputs for use later.
    HRESULT hr = S_OK;
    
    if (pidlFolder)
    {
        m_pidlFolder = ILClone(pidlFolder);   // Make a copy to use later.
        hr = m_pidlFolder ? S_OK : E_OUTOFMEMORY;
    }
    
    if (SUCCEEDED(hr))
    {
        // If a data object pointer was passed into the method, save it and
        // extract the file name. 
        if (pDataObject) 
        { 
            m_pdtobj = pDataObject; 
            m_pdtobj->AddRef(); 
        }
    
        // It is uncommon to use the registry handle, but if you need it,
        // duplicate it now.
        if (hRegKey)
        {
            LSTATUS const result = RegOpenKeyEx(hRegKey, NULL, 0, KEY_READ, &m_hRegKey); 
            hr = HRESULT_FROM_WIN32(result);
        }
    }
    
    return hr;
}
```



## <a name="infotip-customization"></a>Personnalisation de l’info-bulle

Il existe deux façons de personnaliser info-bulles. L’une des méthodes consiste à implémenter un objet qui prend en charge [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) , puis à inscrire l’objet sous la sous-clé appropriée dans le registre (voir ci-dessous). Vous pouvez également spécifier une chaîne fixe ou une liste de certaines propriétés de fichier à afficher.

Pour afficher une chaîne fixe pour une extension d’espace de noms, créez une sous-clé appelée **info-bulle** sous la clé CLSID de votre extension d’espace de noms. Définissez les données de cette sous-clé pour qu’elles soient la chaîne que vous souhaitez afficher.

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Pour afficher une chaîne fixe pour un type de fichier, créez une sous-clé appelée **info-bulle** sous la clé **ProgID** du type de fichier pour lequel vous souhaitez fournir des info-bulles. Définissez les données de cette sous-clé pour qu’elles soient la chaîne que vous souhaitez afficher.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

Si vous souhaitez que l’interpréteur de commandes affiche certaines propriétés de fichier dans l’info-bulle pour un type de fichier spécifique, créez une sous-clé appelée **info-bulle** sous la clé **ProgID** de ce type de fichier. Définissez les données de cette sous-clé comme une liste délimitée par des points-virgules de noms de propriété canoniques ou {fmtid}, paires PID où *propName* est un nom de propriété canonique et *{fmtid}, PID* est une [**paire fmtid/PID**](./objects.md).

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

Les noms de propriétés suivants peuvent être utilisés.



| Nom de la propriété    | Description                   | Récupéré à partir de                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| Auteur           | Auteur du document        | [**\_auteur PIDSI**](../stg/the-summary-information-property-set.md)                             |
| Intitulé            | Titre du document         | [**\_titre PIDSI**](../stg/the-summary-information-property-set.md)                              |
| Objet          | Résumé de l’objet               | [**PIDSI \_ objet**](../stg/the-summary-information-property-set.md)                            |
| Commentaire          | Commentaires sur le document             | [**PIDSI \_**](../stg/the-summary-information-property-set.md) Propriétés d’un commentaire ou d’un dossier/lecteur |
| PageCount        | Nombre de pages               | [**PIDSI \_ PageCount**](../stg/the-summary-information-property-set.md)                          |
| Nom             | Nom convivial                 | Affichage des dossiers standard                                                                      |
| OriginalLocation | Emplacement du fichier d’origine     | Dossier porte-documents et dossier Corbeille                                                   |
| DateDeleted      | Date de suppression du fichier         | Dossier Corbeille                                                                        |
| Type             | Type de fichier                  | Mode Détails du dossier standard                                                              |
| Taille             | Taille du fichier                  | Mode Détails du dossier standard                                                              |
| SyncCopyIn       | Identique à OriginalLocation      | Identique à OriginalLocation                                                                  |
| Modifié le         | Date de dernière modification            | Mode Détails du dossier standard                                                              |
| Date de création          | Date de création                  | Mode Détails du dossier standard                                                              |
| Atteint         | Date du dernier accès            | Mode Détails du dossier standard                                                              |
| Indossier         | Répertoire contenant le fichier | Résultats de la recherche de documents                                                                   |
| Rank             | Qualité de la recherche de correspondance       | Résultats de la recherche de documents                                                                   |
| FreeSpace        | Espace de stockage disponible       | Lecteurs de disque                                                                               |
| NumberOfVisits   | Nombre de visites              | Dossier Favoris                                                                          |
| Attributs       | Attributs de fichier               | Mode Détails du dossier standard                                                              |
| Company          | Nom de la société                  | [**\_entreprise PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Category         | Catégorie de document             | [**\_catégorie PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| copyright        | Copyright du support               | [**\_Copyright PIDMSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| HTMLInfoTipFile  | Fichier info-bulle HTML             | Fichier Desktop.ini pour le dossier                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription des gestionnaires d’extensions de Shell](reg-shell-exts.md)
</dt> </dl>

 

 
