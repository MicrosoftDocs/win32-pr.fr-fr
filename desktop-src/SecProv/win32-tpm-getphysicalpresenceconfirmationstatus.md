---
description: Indique si la confirmation d’un utilisateur physiquement présent est requise pour une opération de présence physique donnée.
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: 'Win32_Tpm :: GetPhysicalPresenceConfirmationStatus, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceConfirmationStatus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 61dc2798973a82cfc75c803f2bf8307c8a43b3c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952370"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a>Win32 \_ TPM :: GetPhysicalPresenceConfirmationStatus, méthode

Indique si la confirmation d’un utilisateur physiquement présent est requise pour une opération de présence physique donnée.

Cette méthode est accessible uniquement par les administrateurs locaux.

## <a name="syntax"></a>Syntaxe


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Opération* \[ dans\]
</dt> <dd>

Valeur entière qui spécifie l’opération TPM demandée qui requiert une présence physique. Les commandes spécifiques au fournisseur sont également prises en charge.

Le paramètre d' *opération* peut comprendre les valeurs suivantes.



| Valeur                                                                                                                               | Signification                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>1</dt> </dl>                                                        | Activer<br/>                                        |
| <dl> <dt>2</dt> </dl>                                                        | Désactiver<br/>                                       |
| <dl> <dt>3</dt> </dl>                                                        | Activer<br/>                                      |
| <dl> <dt>4</dt> </dl>                                                        | Désactivation<br/>                                    |
| <dl> <dt>5</dt> </dl>                                                        | Effacer<br/>                                         |
| <dl> <dt>6</dt> </dl>                                                        | Activer + activer<br/>                             |
| <dl> <dt>7</dt> </dl>                                                        | Désactiver + désactiver<br/>                          |
| <dl> <dt>8</dt> </dl>                                                        | SetOwnerInstall \_ true<br/>                         |
| <dl> <dt>9</dt> </dl>                                                        | SetOwnerInstall \_ false<br/>                        |
| <dl> <dt>10</dt> </dl>                                                       | Enable + Activate + SetOwnerInstall \_ true<br/>     |
| <dl> <dt>11</dt> </dl>                                                       | SetOwnerInstall \_ false + Deactivate + Disable<br/> |
| <dl> <dt></dt><dt>12</dt> </dl> | PresenceunownedFieldUpgrade physique différé<br/> |
| <dl> <dt></dt><dt>14</dt> </dl> | Clear + activer + activer<br/>                     |
| <dl> <dt>15</dt> </dl>                                                       | SetNoPPIProvision \_ false<br/>                      |
| <dl> <dt>16</dt> </dl>                                                       | SetNoPPIProvision \_ true<br/>                       |
| <dl> <dt>17</dt> </dl>                                                       | SetNoPPIClear \_ false<br/>                          |
| <dl> <dt>19</dt> </dl>                                                       | SetNoPPIClear \_ true<br/>                           |
| <dl> <dt>19</dt> </dl>                                                       | SetNoPPIMaintenance \_ false<br/>                    |
| <dl> <dt>20</dt> </dl>                                                       | SetNoPPIMaintenance \_ true<br/>                     |
| <dl> <dt>21</dt> </dl>                                                       | Activer + activer + effacer<br/>                     |
| <dl> <dt>22</dt> </dl>                                                       | Activer + activer + effacer + activer + activer<br/> |



 

</dd> <dt>

*ConfirmationStatus* \[ à\]
</dt> <dd>

Retourne l’état de confirmation de la commande de présence physique.

Le paramètre *ConfirmationStatus* peut contenir les valeurs suivantes.



| Valeur                                                                        | Signification                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Non implémenté<br/>                                             |
| <dl> <dt>1</dt> </dl> | BIOS uniquement.<br/>                                                  |
| <dl> <dt>2</dt> </dl> | Bloqué pour le système d’exploitation par la configuration du BIOS.<br/> |
| <dl> <dt>3</dt> </dl> | Utilisateur autorisé et physiquement présent requis.<br/>               |
| <dl> <dt>4</dt> </dl> | Utilisateur autorisé et physiquement présent non requis<br/>            |



 

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

 

 
