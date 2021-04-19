---
description: Créez un nouvel élément enfant. Ajoute des objets IWiaItem2 à l’arborescence IWiaItem2 d’un appareil.
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: 'IWiaItem2 :: CreateChildItem, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CreateChildItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0002a6110894491a8d6efabb5a142b7c81adc820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517718"
---
# <a name="iwiaitem2createchilditem-method"></a>IWiaItem2 :: CreateChildItem, méthode

Créez un nouvel élément enfant. Ajoute des objets [**IWiaItem2**](-wia-iwiaitem2.md) à l’arborescence **IWiaItem2** d’un appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateChildItem(
  [in]  LONG      lItemFlags,
  [in]  LONG      lCreationFlags,
  [in]  BSTR      bstrItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lItemFlags* \[ dans\]
</dt> <dd>

Type : **long**

Spécifie le type d’élément WIA 2,0. Consultez [**indicateurs de type d’élément WIA**](-wia-wia-item-type-flags.md).

</dd> <dt>

*lCreationFlags* \[ dans\]
</dt> <dd>

Type : **long**

Spécifie comment créer le nouvel élément.

<dt>

<span id="0"></span>

<span id="0"></span>**0** (0)


</dt> <dd>

Définissez les valeurs par défaut des propriétés de l’enfant.

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**Copier \_ \_ \_ Valeurs de propriété Parent** (0x40000000)


</dt> <dd>

Copiez les valeurs de toutes les propriétés en lecture/écriture à partir du parent.

</dd> </dl> </dd> <dt>

*bstrItemName* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie le nom de l’élément. Ce nom est ajouté à la fin du nom de l’élément parent pour générer le nom complet de l’élément.

</dd> <dt>

*ppIWiaItem2* \[ à\]
</dt> <dd>

Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Reçoit l’adresse d’un pointeur vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) qui définit la méthode **IWiaItem2 :: CreateChildItem** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Certains périphériques matériels WIA 2,0 permettent aux applications de créer des éléments dans l’arborescence [**IWiaItem2**](-wia-iwiaitem2.md) qui représente l’appareil. Les applications doivent tester les périphériques pour voir s’ils prennent en charge cette fonctionnalité. Utilisez l' \_ interface IEnumWIA dev \_ Caps pour énumérer les fonctionnalités actuelles de l’appareil.

Si l’appareil autorise la création de nouveaux éléments dans l’arborescence [**IWiaItem2**](-wia-iwiaitem2.md) , l’appel de **IWiaItem2 :: CreateChildItem** crée un nouvel objet **IWiaItem2** qui est un enfant du nœud actuel. Il passe un pointeur vers le nouveau nœud à l’application via le paramètre *ppIWiaItem2* . Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIWiaItem2* .

Si *lCreationFlags* est une \_ copie \_ \_ des valeurs de propriété parent et *lItemFlags* est égal à zéro, la fonction retourne E \_ INVALIDARG.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
