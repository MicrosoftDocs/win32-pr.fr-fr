---
title: Méthode ISoftKbd CreateSoftKeyboardLayoutFromResource (Softkbdc. h)
description: La méthode ISoftKbd CreateSoftKeybboardLayoutFromResource crée une disposition de clavier programmable à partir de la ressource spécifiée.
ms.assetid: c1b2f8bd-8065-426d-9c23-67fa46a33dc8
keywords:
- Infrastructure des services de texte de méthode CreateSoftKeyboardLayoutFromResource
- CreateSoftKeyboardLayoutFromResource méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode CreateSoftKeyboardLayoutFromResource
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromResource
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f454b5d8f3366517d91170d6a92d6a9dbed5764
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511163"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromresource-method"></a>ISoftKbd :: CreateSoftKeyboardLayoutFromResource, méthode

La méthode **ISoftKbd :: CreateSoftKeybboardLayoutFromResource** crée une disposition de clavier logiciel à partir de la ressource spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateSoftKeyboardLayoutFromResource(
  [in]  WCHAR *lpszResFile,
  [in]  WCHAR *lpszResType,
  [in]  WCHAR *lpszXMLResString,
  [out] DWORD *lpdwLayoutCookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszResFile* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par zéro indiquant le nom du fichier de ressources.

</dd> <dt>

*lpszResType* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par zéro indiquant le type de ressource.

</dd> <dt>

*lpszXMLResString* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par zéro qui identifie la ressource.

</dd> <dt>

*lpdwLayoutCookie* \[ à\]
</dt> <dd>

Pointeur vers la mémoire tampon dans laquelle cette méthode récupère un cookie de disposition de clavier programmable.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                        | Description                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Un ou plusieurs paramètres ne sont pas valides.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| MIDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)
</dt> <dt>

[**ISoftKbd::ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)
</dt> </dl>

 

 





