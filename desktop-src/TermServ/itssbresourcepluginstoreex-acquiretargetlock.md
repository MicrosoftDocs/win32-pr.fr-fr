---
title: Méthode ITsSbResourcePluginStoreEx AcquireTargetLock
description: Verrouille une cible.
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AcquireTargetLock
- Méthode AcquireTargetLock Services Bureau à distance, interface ITsSbResourcePluginStoreEx
- Services Bureau à distance de l’interface ITsSbResourcePluginStoreEx, méthode AcquireTargetLock
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.AcquireTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c18be0a544ebcea2d2cecb40dcea3a08e4bd35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103156"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a>ITsSbResourcePluginStoreEx :: AcquireTargetLock, méthode

Verrouille une cible.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AcquireTargetLock(
  [in]  BSTR     targetName,
  [in]  DWORD    dwTimeout,
  [out] IUnknown **ppContext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TargetName* \[ dans\]
</dt> <dd>

Nom de la cible à verrouiller.

</dd> <dt>

*dwTimeout* \[ dans\]
</dt> <dd>

Délai d’attente de l’opération, en millisecondes.

</dd> <dt>

*ppContext* \[ à\]
</dt> <dd>

Retourne un pointeur vers le contexte du verrou. Pour libérer le verrou, fournissez ce pointeur à la méthode [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Une fois le verrou acquis, le thread appelant est supposé avoir un accès exclusif à l’objet cible et, par conséquent, aucun autre thread (au sein du même ordinateur) ne peut le mettre à jour. Par conséquent, le thread appelant doit appeler la méthode [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) dès qu’il a effectué les mises à jour nécessaires de l’objet cible.

> [!IMPORTANT]
> ce verrou n’empêche pas complètement la modification des objets cibles en externe s’il existe plusieurs Service Broker pour les connexions dans le déploiement. Le thread appelant doit être prêt à gérer une défaillance de manière appropriée et à retenter la mise à jour cible.

 

Cette méthode est disponible sur Windows Server 2012 R2 avec [KB3091411](https://support.microsoft.com/kb/3091411) installé dans l’interface [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                             |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2012 R2<br/>                                                             |
| MIDL<br/>                      | <dl> <dt>SbTsV. idl</dt> </dl>          |
| IID<br/>                      | IID \_ ITsSbResourcePluginStoreEx est défini en tant que 80b83ffd-625d-11e5-BEA1-a0481c7e9064<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





