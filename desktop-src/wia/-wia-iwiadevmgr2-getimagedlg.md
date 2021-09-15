---
description: 'la méthode IWiaDevMgr2 :: GetImageDlg affiche une ou plusieurs boîtes de dialogue qui permettent à un utilisateur d’acquérir une image à partir d’un appareil WIA (Windows image Acquisition) 2,0 et d’écrire l’image dans un fichier spécifié.'
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: 'IWiaDevMgr2 :: GetImageDlg, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.GetImageDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6777b839beeb809383e524960e8882392be4bd24
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524033"
---
# <a name="iwiadevmgr2getimagedlg-method"></a>IWiaDevMgr2 :: GetImageDlg, méthode

la méthode **IWiaDevMgr2 :: GetImageDlg** affiche une ou plusieurs boîtes de dialogue qui permettent à un utilisateur d’acquérir une image à partir d’un appareil WIA (Windows image Acquisition) 2,0 et d’écrire l’image dans un fichier spécifié. Cette méthode étend les fonctionnalités de [**IWiaDevMgr2 :: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) pour encapsuler l’acquisition d’images dans un seul appel d’API.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetImageDlg(
  [in]      LONG      lFlags,
  [in]      BSTR      bstrDeviceID,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in]      BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppItem
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Spécifie le comportement de la boîte de dialogue. Peut être défini avec les valeurs suivantes :



| Indicateur                                 | Signification                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Comportement par défaut                                                                                                                                                           |
| \_boîte de dialogue de l’appareil WIA \_ \_ utiliser \_ \_ l’interface utilisateur commune | Utilisez l’interface utilisateur du système au lieu de l’interface utilisateur fournie par le fournisseur. Si l’interface utilisateur système n’est pas disponible, l’interface utilisateur du fournisseur est utilisée. Si aucune interface utilisateur n’est disponible, la fonction retourne E \_ NOTIMPL. |



 

</dd> <dt>

*bstrDeviceID* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie le scanneur à utiliser.

</dd> <dt>

*hwndParent* \[ dans\]
</dt> <dd>

Type : **HWND**

Handle de la fenêtre qui possède la boîte de dialogue **obtenir l’image** .

</dd> <dt>

*bstrFolderName* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie le nom du dossier ITO qui stocke les fichiers analysés dans.

</dd> <dt>

*bstrFilename* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie le nom du fichier dans lequel écrire les données de l’image.

</dd> <dt>

*plNumFiles* \[ dans\]
</dt> <dd>

Type : **long \***

Pointeur vers le nombre de fichiers à analyser.

</dd> <dt>

*ppbstrFilePaths* \[ dans\]
</dt> <dd>

Type : **BSTR \* \***

Adresse d’un pointeur vers un tableau de chemins d’accès pour les fichiers analysés. Initialisez le pointeur pour pointer vers un tableau de taille zéro (0) avant l’appel de **IWiaDevMgr2 :: GetImageDlg** . Consultez la **section Notes**.

</dd> <dt>

*ppItem* \[ in, out\]
</dt> <dd>

Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Adresse d’un pointeur vers le [**IWiaItem2**](-wia-iwiaitem2.md) à partir duquel les images ont été analysées.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

**IWiaDevMgr2 :: GetImageDlg** retourne s \_ OK si les données sont transférées avec succès, retourne \_ la valeur false si l’utilisateur annule la boîte de dialogue ou retourne une erreur com standard.

> [!Note]  
> Le paramètre *ppbstrFilePaths* n’est pas nécessairement vide si la fonction retourne S \_ false. Si l’utilisateur annule, les pages dont l’analyse est terminée sont traitées et retournées dans *ppbstrFilePaths*. Même s’ils ne sont pas utilisés, vous devez libérer le tableau. Consultez la **section Notes**.

 

## <a name="remarks"></a>Notes

Si l’application transmet **null** pour la valeur du paramètre *bstrDeviceID* , **IWiaDevMgr2 :: GetImageDlg** affiche la boîte de dialogue **Sélectionner un appareil** afin que l’utilisateur puisse sélectionner l’appareil d’entrée WIA 2,0.

Utilisez un élément de menu nommé **à partir de scanner** dans le menu **fichier** pour que les sélections d’appareil et d’image soient disponibles dans votre application.

Appelez [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) sur chaque BSTR du tableau sur lequel *ppbstrFilePaths* \[ i \] pointe, puis appelez [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) sur le tableau lui-même pour libérer de la mémoire associée. Si S \_ false est retourné, vérifiez si la valeur vers laquelle pointe *plNumFiles* est différente de zéro. Si la valeur n’est pas égale à zéro, libérez les ressources *ppbstrFilePaths* \[ i \] dans l’application, car l’utilisateur peut annuler après avoir analysé une ou plusieurs pages. Initialisez *plNumFiles* sur zéro avant d’appeler **IWiaDevMgr2 :: GetImageDlg**. Si *plNumFiles* n’est pas initialisé à zéro et qu’une défaillance dans l’infrastructure com entraîne le retour de S \_ false par la fonction avant l’appel de **IWiaDevMgr2 :: GetImageDlg** , *plNumFiles* aura une valeur de garbage collector trompeuse.

La boîte de dialogue doit avoir des droits suffisants sur *bstrFolderName* pour pouvoir enregistrer les fichiers avec des noms de fichiers uniques. Protégez le dossier à l’aide d’une liste de contrôle d’accès (ACL), car il contient des données utilisateur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 
