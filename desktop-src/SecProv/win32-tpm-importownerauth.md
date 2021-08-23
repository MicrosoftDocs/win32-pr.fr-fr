---
description: Importe les informations d’autorisation du propriétaire pour un module de plateforme sécurisée qui est déjà détenu dans le Registre du système d’exploitation.
ms.assetid: 9611D363-6F10-48B9-B417-97133E975257
title: 'Win32_Tpm :: ImportOwnerAuth, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ImportOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6e7d96a5cadf77e539d703ed95f428fa91535d49d1e7b5581300467782fce0af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004077"
---
# <a name="win32_tpmimportownerauth-method"></a>Win32 \_ TPM :: ImportOwnerAuth, méthode

Importe les informations d’autorisation du propriétaire pour un module de plateforme sécurisée qui est déjà détenu dans le Registre du système d’exploitation. Cette opération va tout d’abord vérifier si les informations d’autorisation du propriétaire fournies sont correctes. Si elle est correcte, la méthode importe ces informations dans le registre.

Cette méthode est accessible uniquement par les administrateurs locaux.

## <a name="syntax"></a>Syntaxe


```C++
uint32 ImportOwnerAuth(
  [in] STRING OwnerAuth
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Origine* \[ dans\]
</dt> <dd>

Informations d’autorisation du propriétaire valides pour le module de plateforme sécurisée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux [services de base TPM](../tbs/tbs-return-codes.md) , peuvent être retournées.

Les codes de retour courants sont répertoriés ci-dessous.



| Code/valeur de retour                                                                                                                                 | Description                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode est particulièrement utile dans les scénarios où le module de plateforme sécurisée est dans un état « prêt à fonctionner avec des fonctionnalités réduites » et nécessite que l’importation de l’autorisation du propriétaire soit entièrement prête ou dans un scénario à double démarrage où l’un des systèmes d’exploitation possédait le TPM et que les informations d’autorisation du propriétaire du module de plateforme sécurisée ne sont pas disponibles

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

 

 
