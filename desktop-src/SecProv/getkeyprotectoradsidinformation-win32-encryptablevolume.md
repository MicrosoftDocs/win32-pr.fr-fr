---
description: Récupère l’identificateur de sécurité et les indicateurs utilisés pour protéger une clé.
ms.assetid: 5EF97F44-78FF-4FBF-9142-F2DD0A849057
title: Méthode GetKeyProtectorAdSidInformation de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 57e72488a9e53f49383d179b0bcb1a8b9ff1f706
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "106542812"
---
# <a name="getkeyprotectoradsidinformation-method-of-the-win32_encryptablevolume-class"></a>Méthode GetKeyProtectorAdSidInformation de la \_ classe Win32 EncryptableVolume

La méthode **GetKeyProtectorAdSidInformation** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) récupère l’identificateur de sécurité et les indicateurs utilisés pour protéger une clé.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] string SidString,
  [out] uint32 Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VolumeKeyProtectorID* \[ dans\]
</dt> <dd>

Type : **chaîne**

Identificateur de chaîne qui peut être utilisé pour gérer un protecteur de clé de volume chiffré.

</dd> <dt>

*SidString* \[ à\]
</dt> <dd>

Type : **chaîne**

Chaîne qui contient l’identificateur de sécurité (SID).

</dd> <dt>

*Indicateurs* \[ à\]
</dt> <dd>

Type : **UInt32**

Indicateurs qui modifient le comportement de la fonction. Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                                                     | Signification                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <dt>**FVE \_ \_Indicateur DPAPI \_ ng \_ aucun**</dt> <dt>0x0000</dt> </dl>                                                                   | Aucun effet.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <dt>**FVE \_ \_ \_ Indicateur \_ de déverrouillage de l’indicateur GN GN \_ en tant que \_ \_ compte de service**</dt> <dt>0x0001</dt> </dl> | Spécifie que le protecteur basé sur SID a été protégé sur un compte de service. Si cet indicateur est spécifié, l’appelant doit s’assurer qu’il s’exécute en tant que compte de service approprié avant d’appeler [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (en supprimant temporairement l’emprunt d’identité, par exemple).<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 entreprise, applications de bureau Windows 8 professionnel \[ uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
