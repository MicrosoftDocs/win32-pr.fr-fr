---
title: ITsSbTarget propriété TargetLoad
description: Récupère le chargement relatif sur une cible.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété TargetLoad
- Services Bureau à distance de la propriété TargetLoad, interface ITsSbTarget
- Services Bureau à distance de l’interface ITsSbTarget, propriété TargetLoad
- Services Bureau à distance de la propriété TargetLoad, interface ITsSbTargetEx
- Services Bureau à distance de l’interface ITsSbTargetEx, propriété TargetLoad
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetLoad
- ITsSbTarget.get_TargetLoad
- ITsSbTargetEx.TargetLoad
- ITsSbTargetEx.get_TargetLoad
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d6d4839f60ef4b4af33498658bd78bf234c14f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482345"
---
# <a name="itssbtargettargetload-property"></a>ITsSbTarget :: TargetLoad, propriété

Récupère le chargement relatif sur une cible. Cette valeur est basée sur le nombre de sessions existantes et en attente. Par défaut, une session en attente a la même valeur qu’une session existante.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a>Valeur de la propriété

Nombre représentant la charge relative sur une cible.

## <a name="remarks"></a>Remarques

Le poids d’une session en attente par rapport à une session active peut être modifié en définissant la valeur du paramètre *lb \_ ConnectionEstablishmentPenalty* pour le Service Broker pour les connexions. Ce paramètre se trouve sous la clé de Registre **HKLM \\ System \\ CurrentControlSet \\ services \\ Tssdis \\ Parameters** . La valeur par défaut 1 indique que les sessions en attente ont le même poids que les sessions actives.

cette propriété est disponible sur Windows Server 2012 R2 avec [KB3091411](https://support.microsoft.com/kb/3091411) installé dans l’interface [**ITsSbTargetEx**](itssbtargetex.md) .

## <a name="requirements"></a>Configuration requise




| | | Client minimal pris en charge<br /> | Aucun pris en charge<br /> | | Serveur minimal pris en charge<br /> | Windows Server 2016<br /> | | MIDL<br /> | <dl><dt>Sbtsv. idl</dt></dl> | | VAUT<br /> | IID_ITsSbTarget est défini comme suit :<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 sur Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





