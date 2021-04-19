---
description: Obtient l’empreinte numérique de la clé racine de stockage pour un module donné de la partie publique de la clé racine de stockage GPC.
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
ms.openlocfilehash: 81e1ec53596a3d5ce469d412e9bd7ca17e1ad8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536327"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a>Win32 \_ TPM :: GetSrkADThumbprint, méthode

Obtient l’empreinte numérique de la clé racine de stockage pour un module donné de la partie publique de la clé racine de stockage GPC. L’empreinte numérique est utilisée pour indexer les clés de racine de stockage sur le serveur de Active Directory si la sauvegarde Active Directory des informations d’autorisation du propriétaire du module de plateforme sécurisée est activée via le paramètre stratégie de groupe.

> [!Note]  
> À partir de Windows 10, version 1607, l’autorisation du propriétaire du module de plateforme sécurisée n’est jamais sauvegardée dans Active Directory.

 

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

Modulo de la partie publique de la clé racine de stockage GPC. Elle peut également être obtenue à l’aide de la méthode [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) de la classe [ \_ TPM Win32](win32-tpm.md) .

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



 

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                      |
| Espace de noms<br/>                | \\\\.\\ racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>\_TPM. mof Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
