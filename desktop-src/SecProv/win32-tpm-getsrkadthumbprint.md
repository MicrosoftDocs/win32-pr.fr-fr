---
description: obtient l’empreinte numérique de la clé racine Stockage pour un module donné de la partie publique de la clé racine du module de plateforme sécurisée Stockage.
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: 'Win32_Tpm :: GetSrkADThumbprint, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkADThumbprint
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 9be4b7f02a9b645c29b431a9d974f5871ad5a95fc001e43df17bfe459483974e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004107"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a>Win32 \_ TPM :: GetSrkADThumbprint, méthode

obtient l’empreinte numérique de la clé racine Stockage pour un module donné de la partie publique de la clé racine du module de plateforme sécurisée Stockage. l’empreinte numérique est utilisée pour indexer les clés racines de Stockage sur le serveur Active Directory si la Active Directory sauvegarde des informations d’autorisation du propriétaire du module de plateforme sécurisée est activée via le paramètre stratégie de groupe.

> [!Note]  
> à partir de Windows 10, la version 1607, l’autorisation du propriétaire du module de plateforme sécurisée n’est jamais sauvegardée dans Active Directory.

 

Cette méthode est accessible uniquement par les administrateurs locaux.

## <a name="syntax"></a>Syntaxe


```C++
uint32 GetSrkADThumbprint(
  [in]  uint8 SrkPublicKeyModulus,
  [out] uint8 SrkADThumbprint
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SrkPublicKeyModulus* \[ dans\]
</dt> <dd>

le module de la partie publique de la clé racine du module de plateforme sécurisée Stockage. Elle peut également être obtenue à l’aide de la méthode [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) de la classe [ \_ TPM Win32](win32-tpm.md) .

</dd> <dt>

*SrkADThumbprint* \[ à\]
</dt> <dd>

Retourne un tableau de 20 octets contenant l’empreinte numérique de la clé racine de stockage pour le modulo donné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux [services de base TPM](../tbs/tbs-return-codes.md) , peuvent être retournées.

Les codes de retour courants sont répertoriés ci-dessous.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Remarques

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                      |
| Espace de noms<br/>                | \\\\.\\ racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>\_TPM. mof Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
