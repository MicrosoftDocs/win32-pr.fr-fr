---
description: Indique l’action de l’utilisateur nécessaire pour effectuer l’opération de présence physique Module de plateforme sécurisée (TPM) (TPM). Utilisez la méthode SetPhysicalPresenceRequest pour demander une opération.
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: Méthode GetPhysicalPresenceTransition de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceTransition
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 4e6a3ab2295cc26cd439465b569f594dd1e0580a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534680"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a>Méthode GetPhysicalPresenceTransition de la \_ classe TPM Win32

La méthode **GetPhysicalPresenceTransition** de la [**classe \_ TPM Win32**](win32-tpm.md) indique l’action de l’utilisateur nécessaire pour effectuer l’opération de présence physique module de plateforme sécurisée (TPM) (TPM). Utilisez la méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) pour demander une opération. L’action utilisateur requise est définie pour votre ordinateur au moment de la fabrication. En règle générale, un redémarrage de l’ordinateur est nécessaire.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Transition* \[ à\]
</dt> <dd>

Type : **UInt32**

Valeur entière qui spécifie la transition nécessaire pour effectuer une opération de présence physique TPM.



| Valeur                                                                        | Signification                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Aucune action de l’utilisateur n’est nécessaire pour effectuer une opération de présence physique TPM.<br/>                                                                                                                                                                              |
| <dl> <dt>1</dt> </dl> | Pour effectuer une opération de présence physique TPM, l’utilisateur doit arrêter l’ordinateur, puis le réactiver à l’aide du bouton d’alimentation. L’utilisateur doit être physiquement présent sur l’ordinateur pour accepter ou refuser la modification quand le BIOS le demande.<br/> |
| <dl> <dt>2</dt> </dl> | Pour effectuer une opération de présence physique TPM, l’utilisateur doit redémarrer l’ordinateur à l’aide d’un redémarrage à chaud. L’utilisateur doit être physiquement présent sur l’ordinateur pour accepter ou refuser la modification quand le BIOS le demande.<br/>                              |
| <dl> <dt>3</dt> </dl> | L’action requise de l’utilisateur est inconnue.<br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.

Le tableau suivant répertorie certains des codes de retour courants.



| Code/valeur de retour                                                                                                                                                                      | Description                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                      | La méthode a réussi.<br/>                                                            |
| <dl> <dt>**Module TPM \_ \_ \_ \_ Erreur ACPI PPP**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Une défaillance matérielle s’est produite. Pour plus d'informations, consultez le fabricant de votre ordinateur.<br/> |



 

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                      |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM. mof Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
