---
description: Retourne les résultats d’une opération de présence physique TPM effectuée.
ms.assetid: 28d76149-3905-45db-a41e-32fac1603582
title: Méthode GetPhysicalPresenceResponse de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceResponse
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5f32379c9e0f538c2f9be4466b55158d0abcdd51a4d2612634b2b03ff869ed41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891859"
---
# <a name="getphysicalpresenceresponse-method-of-the-win32_tpm-class"></a>Méthode GetPhysicalPresenceResponse de la \_ classe TPM Win32

La méthode **GetPhysicalPresenceResponse** de la [**classe \_ TPM Win32**](win32-tpm.md) retourne les résultats d’une opération de présence physique TPM qui a été effectuée. Utilisez la méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) pour demander une opération.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetPhysicalPresenceResponse(
  [out] uint32 Request,
  [out] uint32 Response
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Demande* \[ à\]
</dt> <dd>

Type : **UInt32**

Valeur entière qui spécifie l’opération de présence physique TPM effectuée.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt>entre</dt> </dl></td>
<td>Aucune demande.<br/> Aucune opération de présence physique n’a été effectuée.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>1</dt> </dl></td>
<td>Activez le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 2. <br/> Pour plus d’informations, consultez les méthodes associées qui n’impliquent pas de présence physique :
<ul>
<li><a href="enable-win32-tpm.md"><strong>Activer</strong></a></li>
<li><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>2</dt> </dl></td>
<td>Désactivez le module TPM.<br/> Cette opération est inversée par l’opération 1. <br/> Pour plus d’informations, consultez cette méthode associée qui n’implique pas de présence physique : <a href="disable-win32-tpm.md"><strong>Désactiver</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>1,3</dt> </dl></td>
<td>Activez le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 4.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>4</dt> </dl></td>
<td>Désactivez le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 3.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>5,5</dt> </dl></td>
<td>Effacez le module de plateforme sécurisée.<br/> Cette opération ne peut pas être inversée. <br/> Pour plus d’informations, consultez cette méthode associée qui n’implique pas la présence physique : <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>6,3</dt> </dl></td>
<td>Activez et activez le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 7.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>Commission(7</dt> </dl></td>
<td>Désactivez et désactivez le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 6. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>version8</dt> </dl></td>
<td>Autorise l’installation d’un propriétaire de module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 9.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>0,9</dt> </dl></td>
<td>Empêche l’installation d’un propriétaire de module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 8. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>10</dt> </dl></td>
<td>Activer, activer et autoriser l’installation d’un propriétaire TPM.<br/> Cette opération est inversée par l’opération 11.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>11</dt> </dl></td>
<td>Désactivez, désactivez et empêchez l’installation d’un propriétaire de module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 10.<br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <dt><strong></strong></dt><dt>12</dt> </dl></td>
<td>PresenceunownedFieldUpgrade physique différé<br/> Le paramètre de présence physique a été mis à jour.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>14,5</dt> </dl></td>
<td>Désactivez, activez et activez le module de plateforme sécurisée.<br/> Cette opération ne peut pas être inversée.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>4,5</dt> </dl></td>
<td>SetNoPPIProvision_False<br/> Définit la configuration dont vous devez disposer physiquement pour définir le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 16.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>16bits</dt> </dl></td>
<td>SetNoPPIProvision_True<br/> Définit la provision pour laquelle vous n’avez pas besoin d’être physiquement en présence pour définir le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 15.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>17</dt> </dl></td>
<td>SetNoPPIClear_False<br/> Définit la configuration dont vous devez disposer physiquement pour effacer le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 18.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>19</dt> </dl></td>
<td>SetNoPPIClear_True<br/> Définit la provision pour laquelle vous n’avez pas besoin d’être physiquement en présence pour effacer le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 17.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>19</dt> </dl></td>
<td>SetNoPPIMaintenance_False<br/> Définit la configuration dont vous devez disposer physiquement pour gérer le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 20.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>20</dt> </dl></td>
<td>SetNoPPIMaintenance_True<br/> Définit la configuration dont vous devez disposer physiquement pour gérer le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 19.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>21</dt> </dl></td>
<td>Activer + activer + effacer<br/> Activez, activez et désactivez le module de plateforme sécurisée.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>22</dt> </dl></td>
<td>Activer + activer + effacer + activer + activer<br/> Activez, activez et désactivez le module de plateforme sécurisée, puis activez et réactivez le module de plateforme sécurisée.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*Réponse* \[ à\]
</dt> <dd>

Type : **UInt32**

Valeur entière qui spécifie les résultats de l’exécution de l’opération de présence physique TPM.

Une opération de présence physique est réussie si un utilisateur physiquement présent confirme l’opération et si l’opération s’exécute sans erreur.

Cette valeur peut contenir toute erreur TPM. Le tableau suivant répertorie quelques-unes des réponses d’erreur courantes.



| Valeur                                                                                                                                                                                                                                                                    | Signification                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                                                                                                                                                                                             | L’opération TPM demandée a réussi.<br/>              |
| <span id="TPM_E_PPI_USER_ABORT"></span><span id="tpm_e_ppi_user_abort"></span><dl> <dt>**Module TPM \_ E \_ PPP \_ utilisateur \_ Abort**</dt> <dt>2150171393 (0x80290301)</dt> </dl>       | L’utilisateur a refusé l’opération TPM demandée.<br/>           |
| <span id="TPM_E_PPI_BIOS_FAILURE"></span><span id="tpm_e_ppi_bios_failure"></span><dl> <dt>**Module TPM \_ \_ \_ \_ Erreur du BIOS E-PPP**</dt> <dt>2150171394 (0x80290302)</dt> </dl> | Une défaillance du BIOS s’est produite lors de l’exécution de l’opération TPM.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.

Le tableau suivant répertorie certains des codes de retour courants.



| Code/valeur de retour                                                                                                                                                                      | Description                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                      | La méthode a réussi.<br/>                                                            |
| <dl> <dt>**Module TPM \_ \_ \_ \_ Erreur ACPI PPP**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Une défaillance matérielle s’est produite. Pour plus d'informations, consultez le fabricant de votre ordinateur.<br/> |



 

## <a name="remarks"></a>Remarques

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
</dt> <dt>

[**Effacer**](clear-win32-tpm.md)
</dt> <dt>

[**Désactive**](disable-win32-tpm.md)
</dt> <dt>

[**Activer**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> </dl>

 

 
