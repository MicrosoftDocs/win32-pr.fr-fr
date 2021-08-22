---
description: Interrompt les processus du package s’ils sont en cours d’exécution.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: 'IPackageDebugSettings :: suspend, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Suspend
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 0517ce3cca6a8e74f19b053897511062cefa252297d3a0e6633d4678c0deaa95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822812"
---
# <a name="ipackagedebugsettingssuspend-method"></a>IPackageDebugSettings :: suspend, méthode

Interrompt les processus du package s’ils sont en cours d’exécution.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Suspend(
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

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                            | Description                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | L’opération a réussi.<br/>              |
| <dl> <dt>**E \_ STATECHANGE non conforme \_**</dt> </dl> | Le processus n’est pas en cours d’exécution.<br/> |



 

## <a name="remarks"></a>Remarques

Chaque processus reçoit l’événement [**suspension**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) . Il peut être utile pour les développeurs d’effectuer un pas à pas détaillé de la façon dont leurs applications répondent à cet événement.

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

 

 
