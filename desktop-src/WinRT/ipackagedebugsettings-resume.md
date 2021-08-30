---
description: Reprend les processus du package s’ils sont actuellement suspendus.
ms.assetid: c5376e00-b4b7-4a81-a84c-3a46758fe130
title: 'IPackageDebugSettings :: Resume, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Resume
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 6871aea0fc18ce64939fa1bba06946f8a3a1c260e341b1dfa500a71f273a883b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121579"
---
# <a name="ipackagedebugsettingsresume-method"></a>IPackageDebugSettings :: Resume, méthode

Reprend les processus du package s’ils sont actuellement suspendus.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Resume(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*packageFullName* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Nom complet du package.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Chaque processus reçoit l’événement de [**reprise**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) . Il peut être utile pour les développeurs d’effectuer un pas à pas détaillé de la façon dont leurs applications répondent à cet événement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                          |
| MIDL<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))
</dt> </dl>

 

 
