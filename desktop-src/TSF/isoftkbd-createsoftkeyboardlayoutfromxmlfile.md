---
title: Méthode ISoftKbd CreateSoftKeyboardLayoutFromXMLFile (Softkbdc. h)
description: La méthode ISoftKbd CreateSoftKeyboardLayoutFromXMLFile crée une disposition de clavier programmable à partir du fichier XML spécifié.
ms.assetid: e665adab-1d75-4e41-87bf-c8ce0f7a0399
keywords:
- Infrastructure des services de texte de méthode CreateSoftKeyboardLayoutFromXMLFile
- CreateSoftKeyboardLayoutFromXMLFile méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode CreateSoftKeyboardLayoutFromXMLFile
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromXMLFile
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252db845c5e1cc732adc295e1989fee83d4ac6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513808"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromxmlfile-method"></a>ISoftKbd :: CreateSoftKeyboardLayoutFromXMLFile, méthode

La méthode **ISoftKbd :: CreateSoftKeyboardLayoutFromXMLFile** crée une disposition de clavier programmable à partir du fichier XML spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateSoftKeyboardLayoutFromXMLFile(
  [in]  WCHAR *lpszKeyboardDesFile,
  [in]  INT   szFileStrLen,
  [out] DWORD *pdwLayoutCookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszKeyboardDesFile* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par zéro indiquant le nom du fichier XML.

</dd> <dt>

*szFileStrLen* \[ dans\]
</dt> <dd>

Chaîne se terminant par zéro qui indique la longueur du fichier XML.

</dd> <dt>

*pdwLayoutCookie* \[ à\]
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

[**ISoftKbd::CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> </dl>

 

 





