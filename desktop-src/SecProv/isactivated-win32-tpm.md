---
description: La méthode IsActivated de la \_ classe TPM Win32 indique si l’appareil est activé.
ms.assetid: 862c386c-c5b5-44d2-89a5-3735b99bf8bc
title: Méthode IsActivated de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsActivated
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 40399d14d7bbadaab294f7a345d95e6253615c2cd11bd2fe6749edf3deb98be2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906329"
---
# <a name="isactivated-method-of-the-win32_tpm-class"></a>Méthode IsActivated de la \_ classe TPM Win32

La méthode **isActivated** de la [**classe \_ TPM Win32**](win32-tpm.md) indique si l’appareil est activé.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsActivated(
  [out] boolean IsActivated
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IsActivated* \[ à\]
</dt> <dd>

Type : **booléen**

Si la **valeur est true**, l’appareil est activé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.

Les codes de retour courants sont répertoriés ci-dessous.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Remarques

La désactivation est semblable à la désactivation, mais les modifications de l’état opérationnel sont possibles. Conformément à la spécification Trusted Computing Group (TCG) v 1.2, seules les commandes suivantes sont disponibles lorsque l’appareil est dans un état désactivé.

-   \_CONTINUESELFTEST TPM
-   \_DSAP TPM
-   \_FLUSHSPECIFIC TPM
-   \_GETCAPABILITY TPM
-   \_GETTESTRESULT TPM
-   \_Initialisation TPM
-   \_OIAP TPM
-   \_osap TPM
-   \_OWNERSETDISABLE TPM
-   \_Réinitialisation PCR TPM \_
-   \_PHYSICALDISABLE TPM
-   \_PHYSICALENABLE TPM
-   \_PHYSICALSETDEACTIVATED TPM
-   \_Réinitialisation TPM
-   Module de plateforme sécurisée \_ Saacquisition
-   \_SELFTESTFULL TPM
-   \_SETCAPABILITY TPM
-   \_SHA1COMPLETE TPM
-   \_SHA1START TPM
-   \_SHA1UPDATE TPM
-   Démarrage du module de plateforme sécurisée \_
-   \_TAKEOWNERSHIP TPM
-   \_Handle de terminaison TPM \_

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                      |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM. mof Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
