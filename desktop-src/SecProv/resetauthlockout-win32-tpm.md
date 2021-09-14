---
description: Réinitialise le délai d’attente ou tout autre mécanisme que les fabricants de module de plateforme sécurisée implémentent pour se protéger contre les attaques par dictionnaire sur les valeurs d’autorisation TPM.
ms.assetid: c2fba6a2-2d03-4ffd-9841-4a9eac0a20ac
title: Méthode ResetAuthLockOut de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetAuthLockOut
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d28287e410fbaf65ce5b1e617113c35cfece160b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008976"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a>Méthode ResetAuthLockOut de la \_ classe TPM Win32

La méthode **ResetAuthLockOut** de la [**classe \_ TPM Win32**](win32-tpm.md) réinitialise le délai d’attente ou tout autre mécanisme que les fabricants de module de plateforme sécurisée implémentent pour se protéger contre les attaques par dictionnaire sur les valeurs d’autorisation du module de plateforme sécurisée. Dans le cadre d’une attaque par dictionnaire, une personne malveillante tente de deviner une valeur d’autorisation TPM correcte en tentant de façon exhaustive toutes les valeurs possibles.

Utilisez cette méthode si le module de plateforme sécurisée est verrouillé en raison d’un trop grand nombre de tentatives incorrectes lors de l’entrée de l’autorisation du propriétaire ou d’autres valeurs d’autorisation. Lorsque le module de plateforme sécurisée est verrouillé, une partie ou l’ensemble des commandes émises dans le module de plateforme sécurisée (TPM) retournent une erreur, TPM \_ E \_ défendre le \_ verrou \_ en cours d’exécution (0x80280803)

> [!Note]  
> Cette méthode ne peut être utilisée qu’une seule fois lorsque le module de plateforme sécurisée est verrouillé. Si l’autorisation du propriétaire fournie à cette méthode est incorrecte, le module de plateforme sécurisée est verrouillé pour l’intégralité du délai d’attente et les tentatives supplémentaires de réinitialisation du verrou échouent.

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 ResetAuthLockOut(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Origine* \[ dans, facultatif\]
</dt> <dd>

Type : **chaîne**

Chaîne qui identifie le propriétaire du module de plateforme sécurisée.

Cette chaîne doit être une chaîne codée en base64 qui se termine par un caractère null qui contient exactement 20 octets de données binaires. Utilisez la méthode [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) pour convertir une phrase secrète au format attendu. Le paramètre *origine* est lu à partir du Registre si aucun n’est fourni.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées. Le tableau suivant répertorie certaines des valeurs de retour courantes.



| Code/valeur de retour                                                                                                                                                            | Description                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                            | La méthode a réussi.<br/>                                                                                                                                                                                                                                     |
| <dl> <dt>**Module TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl> | La valeur d’autorisation du propriétaire fournie est incorrecte. Les tentatives supplémentaires de réinitialisation du verrou échouent avec la même erreur. Veuillez patienter jusqu’à expiration du délai d’attente ou d’un autre mécanisme propre au fabricant avant de réessayer les commandes TPM verrouillées.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode appelle la \_ commande TPM ResetLockValue sur le module de plateforme sécurisée. Le comportement exact de cette méthode varie selon les fabricants de module de plateforme sécurisée. La documentation du fabricant de l’ordinateur ou du module de plateforme sécurisée peut fournir des informations supplémentaires sur l’implémentation du mécanisme d’attaque anti-dictionnaire.

En général, les fabricants peuvent détecter les attaques par dictionnaire en effectuant le suivi des authentifications ayant échoué. Si le nombre ou la fréquence des échecs est suffisamment élevé, le module de plateforme sécurisée verrouille les commandes supplémentaires pendant un certain temps. En règle générale, le délai d’attente initial sera court, afin de permettre à un utilisateur légitime de corriger la situation. Si les défaillances se poursuivent, la durée de chaque délai d’expiration suivant peut augmenter rapidement.

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

 

 
