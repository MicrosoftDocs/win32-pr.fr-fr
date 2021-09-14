---
description: Retourne l’opération de présence physique TPM en attente. Utilisez la méthode SetPhysicalPresenceRequest pour demander une opération.
ms.assetid: c50378ae-b465-4c82-beb9-8ecb7939dae2
title: Méthode GetPhysicalPresenceRequest de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 7d88ec523e983e60cacab57b41307381b05e8de6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237383"
---
# <a name="getphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Méthode GetPhysicalPresenceRequest de la \_ classe TPM Win32

La méthode **GetPhysicalPresenceRequest** de la [**classe \_ TPM Win32**](win32-tpm.md) retourne l’opération de présence physique TPM en attente. Utilisez la méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) pour demander une opération.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetPhysicalPresenceRequest(
  [out] uint32 Request
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Demande* \[ à\]
</dt> <dd>

Type : **UInt32**

Valeur qui spécifie l’opération de présence physique TPM en attente.




| Valeur | Signification | 
|-------|---------|
| <dl><dt>0</dt></dl> | Aucune demande.<br /> | 
| <dl><dt>1</dt></dl> | Activez le module de plateforme sécurisée.<br /> Cette opération est inversée par l’opération 2. <br /> Pour plus d’informations, consultez les méthodes associées qui n’impliquent pas de présence physique :<ul><li><a href="enable-win32-tpm.md"><strong>Activer</strong></a></li><li><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></li></ul><br /> | 
| <dl><dt>2</dt></dl> | Désactivez le module TPM.<br /> Cette opération est inversée par l’opération 1. <br /> Pour plus d’informations, consultez cette méthode associée qui n’implique pas de présence physique : <a href="disable-win32-tpm.md"><strong>Désactiver</strong></a>.<br /> | 
| <dl><dt>3</dt></dl> | Activez le module de plateforme sécurisée.<br /> Cette opération est inversée par l’opération 4.<br /> | 
| <dl><dt>4</dt></dl> | Désactivez le module de plateforme sécurisée.<br /> Cette opération est inversée par l’opération 3.<br /> | 
| <dl><dt>5</dt></dl> | Effacez le module de plateforme sécurisée.<br /> Cette opération ne peut pas être inversée.<br /> Pour plus d’informations, consultez cette méthode associée qui n’implique pas la présence physique : <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.<br /> | 
| <dl><dt>6</dt></dl> | Activez et activez le module de plateforme sécurisée. <br /> Cette opération est inversée par l’opération 7.<br /> | 
| <dl><dt>7</dt></dl> | Désactivez et désactivez le module de plateforme sécurisée.<br /> Cette opération est inversée par l’opération 6. <br /> | 
| <dl><dt>8</dt></dl> | Autorise l’installation d’un propriétaire de module de plateforme sécurisée. <br /> Cette opération est inversée par l’opération 9.<br /> | 
| <dl><dt>9</dt></dl> | Empêche l’installation d’un propriétaire de module de plateforme sécurisée.<br /> Cette opération est inversée par l’opération 8. <br /> | 
| <dl><dt>10</dt></dl> | Activer, activer et autoriser l’installation d’un propriétaire TPM.<br /> Cette opération est inversée par l’opération 11.<br /> | 
| <dl><dt>11</dt></dl> | Désactivez, désactivez et empêchez l’installation d’un propriétaire de module de plateforme sécurisée.<br /> Cette opération est inversée par l’opération 10.<br /> | 
| <span></span><dl><dt><strong></strong></dt><dt>douze</dt></dl> | PresenceunownedFieldUpgrade physique différé<br /> Le paramètre de présence physique a été mis à jour.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br /> | 
| <dl><dt>14</dt></dl> | Désactivez, activez et activez le module de plateforme sécurisée.<br /> Cette opération ne peut pas être inversée.<br /> | 
| <dl><dt>15</dt></dl> | SetNoPPIProvision_False<br /> Définit la configuration dont vous devez disposer physiquement pour définir le module de plateforme sécurisée.<br /> Cette opération est inversée par l’opération 16.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br /> | 
| <dl><dt>16</dt></dl> | SetNoPPIProvision_True<br /> Définit la provision pour laquelle vous n’avez pas besoin d’être physiquement en présence pour définir le module de plateforme sécurisée.<br /> Cette opération est inversée par l’opération 15.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br /> | 
| <dl><dt>17</dt></dl> | SetNoPPIClear_False<br /> Définit la configuration dont vous devez disposer physiquement pour effacer le module de plateforme sécurisée.<br /> Cette opération est inversée par l’opération 18.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br /> | 
| <dl><dt>19</dt></dl> | SetNoPPIClear_True<br /> Définit la provision pour laquelle vous n’avez pas besoin d’être physiquement en présence pour effacer le module de plateforme sécurisée.<br /> Cette opération est inversée par l’opération 17.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br /> | 
| <dl><dt>19</dt></dl> | SetNoPPIMaintenance_False<br /> Définit la configuration dont vous devez disposer physiquement pour gérer le module de plateforme sécurisée.<br /> Cette opération est inversée par l’opération 20.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br /> | 
| <dl><dt>20</dt></dl> | SetNoPPIMaintenance_True<br /> Définit la configuration dont vous devez disposer physiquement pour gérer le module de plateforme sécurisée.<br /> Cette opération est inversée par l’opération 19.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br /> | 
| <dl><dt>21</dt></dl> | Activer + activer + effacer<br /> Activez, activez et désactivez le module de plateforme sécurisée.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br /> | 
| <dl><dt>22</dt></dl> | Activer + activer + effacer + activer + activer<br /> Activez, activez et désactivez le module de plateforme sécurisée, puis activez et réactivez le module de plateforme sécurisée.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br /> | 




 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.

Le tableau suivant répertorie les codes de retour courants.



| Code/valeur de retour                                                                                                                                                                      | Description                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                      | La méthode a réussi.<br/>                                                            |
| <dl> <dt>**Module TPM \_ \_ \_ \_ Erreur ACPI PPP**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Une défaillance matérielle s’est produite. Pour plus d'informations, consultez le fabricant de votre ordinateur.<br/> |



 

## <a name="remarks"></a>Notes

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Spécifications



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
</dt> <dt>

[**Effacé**](clear-win32-tpm.md)
</dt> <dt>

[**Désactiver**](disable-win32-tpm.md)
</dt> <dt>

[**Activer**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
