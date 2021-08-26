---
description: La méthode PrintXML convertit les données de propriété en une chaîne XML.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: IPropertySetter ::P méthode rintXML (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5070a6906d7f30ab12171f551270f82b9851fa8c3990fade47aca6d2927509be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051509"
---
# <a name="ipropertysetterprintxml-method"></a>IPropertySetter ::P méthode rintXML

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `PrintXML` méthode convertit les données de propriété en une chaîne XML.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszXML* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit la chaîne XML.

</dd> <dt>

*cbXML* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon vers laquelle pointe *pszXML*, en octets.

</dd> <dt>

*pcbPrinted* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit la longueur de la chaîne XML. Peut avoir la **valeur null**.

</dd> <dt>

*mettre en retrait* \[ dans\]
</dt> <dd>

Nombre de niveaux de mise en retrait pour la balise la plus à l’extérieur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite. Sinon, retourne une valeur **HRESULT** indiquant la cause de l’erreur. Si la chaîne XML est plus longue que la mémoire tampon, la méthode retourne E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




