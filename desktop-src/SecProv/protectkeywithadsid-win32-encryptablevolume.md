---
description: Sécurise la clé de chiffrement du volume à l’aide d’un identificateur de sécurité (SID) Active Directory.
ms.assetid: 881EEAF2-49C5-4BBD-B2AA-5E30B61E7D3A
title: Méthode ProtectKeyWithAdSid de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0279a6edc8aaa275fdf75a855452d987de802d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521076"
---
# <a name="protectkeywithadsid-method-of-the-win32_encryptablevolume-class"></a>Méthode ProtectKeyWithAdSid de la \_ classe Win32 EncryptableVolume

La méthode **ProtectKeyWithAdSid** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) sécurise la clé de chiffrement du volume à l’aide d’un identificateur de sécurité (SID) Active Directory.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ProtectKeyWithAdSid(
  [in, optional] string FriendlyName,
  [in]           string SidString,
  [in]           uint32 Flags,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FriendlyName* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui spécifie un identificateur affecté à l’utilisateur pour ce protecteur de clé. Si ce paramètre n’est pas spécifié, une valeur vide est utilisée.

</dd> <dt>

*SidString* \[ dans\]
</dt> <dd>

Chaîne qui contient le SID Active Directory utilisé pour protéger la clé de chiffrement.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Indicateurs qui modifient le comportement de la fonction. Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                                                     | Signification                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <dt>**FVE \_ \_Indicateur DPAPI \_ ng \_ aucun**</dt> <dt>0x0000</dt> </dl>                                                                   | Aucun effet.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <dt>**FVE \_ \_ \_ Indicateur \_ de déverrouillage de l’indicateur GN GN \_ en tant que \_ \_ compte de service**</dt> <dt>0x0001</dt> </dl> | Spécifie que le protecteur basé sur SID a été protégé sur un compte de service. Si cet indicateur est spécifié, l’appelant doit s’assurer qu’il s’exécute en tant que compte de service approprié avant d’appeler [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (en supprimant temporairement l’emprunt d’identité, par exemple).<br/> |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ à\]
</dt> <dd>

Identificateur unique associé au protecteur créé. Vous pouvez utiliser cette chaîne pour gérer le protecteur de clé.

Si le lecteur prend en charge le chiffrement matériel et que BitLocker n’a pas pris possession de la bande, la chaîne d’ID est définie sur « BitLocker » et le protecteur de clé est écrit dans les métadonnées par bande.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md) .

Par défaut, vous ne pouvez pas ajouter à distance un compte Active Directory ou un protecteur de groupe. Vous devez activer la délégation avec restriction sur le contrôleur de domaine et l’ordinateur source. Sur le contrôleur de domaine, procédez comme suit :

1.  Ouvrir le gestionnaire de serveur
2.  Sélectionner les ordinateurs dans Active Directory rôles
3.  Sélectionnez l’ordinateur client cible et cliquez avec le bouton droit
4.  Sélectionner l’onglet délégation
5.  Cochez la case « n’approuver cet ordinateur que pour la délégation aux services spécifiés »
6.  Sélectionnez la case d’option « utiliser Kerberos uniquement »
7.  Cliquez sur Ajouter.
8.  Sélectionnez « utilisateurs ou ordinateurs »
9.  Sélectionner l’hôte/comme nom de principal du service

Effectuez les étapes 3 à 9 sur l’ordinateur source.

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

 

 
