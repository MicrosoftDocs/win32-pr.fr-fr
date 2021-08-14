---
description: Affiche une boîte de dialogue permettant à l’utilisateur de préparer l’acquisition d’images.
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: IWiaItem2 ::D méthode eviceDlg (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c9eaab17f0a76bfc5c6ac919a9abef92ca7288539c9705ca30c02b1dd0a8d1ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118035220"
---
# <a name="iwiaitem2devicedlg-method"></a>IWiaItem2 ::D méthode eviceDlg

Affiche une boîte de dialogue permettant à l’utilisateur de préparer l’acquisition d’images.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeviceDlg(
  [in]      LONG      lFlags,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in, out] BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Spécifie un jeu d’indicateurs qui contrôlent l’opération de la boîte de dialogue. La valeur peut être 0 pour représenter le comportement par défaut ou l’un des \_ indicateurs de boîte de dialogue de périphérique WIA \_ décrits dans [**WiaFlag**](-wia-wiaflag.md).

</dd> <dt>

*hwndParent* \[ dans\]
</dt> <dd>

Type : **HWND**

Handle de la fenêtre parente.

</dd> <dt>

*bstrFolderName* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie le nom du dossier dans lequel les fichiers doivent être transférés.

</dd> <dt>

*bstrFilename* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie le nom du fichier de modèle.

</dd> <dt>

*plNumFiles* \[ dans\]
</dt> <dd>

Type : **long \***

Pointeur vers le nombre d’éléments dans le tableau *ppbstrFilePaths* .

</dd> <dt>

*ppbstrFilePaths* \[ in, out\]
</dt> <dd>

Type : **BSTR \* \***

Adresse d’un pointeur vers un tableau de chemins d’accès pour les fichiers analysés. Initialisez le pointeur pour pointer vers un tableau de taille zéro (0) avant **IWiaItem2 ::D evicedlg** est appelée.

</dd> <dt>

*ppIWiaItem2* \[ in, out\]
</dt> <dd>

Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Adresse d’un tableau de pointeurs vers des interfaces [**IWiaItem2**](-wia-iwiaitem2.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode affiche une boîte de dialogue à l’utilisateur qu’une application utilise pour rassembler toutes les informations requises pour l’acquisition d’images. Il est également utilisé pour spécifier des propriétés d’analyse d’images telles que la luminosité et le contraste.

Une fois que cette méthode a retourné une valeur, l’application peut utiliser l’interface [**IWiaTransfer**](-wia-iwiatransfer.md) pour acquérir l’image.

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour chaque élément du tableau de pointeurs d’interface qu’ils reçoivent via le paramètre *ppIWiaItem2* . Les applications doivent également libérer le tableau à l’aide de [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
