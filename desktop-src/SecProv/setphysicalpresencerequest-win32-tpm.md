---
description: Demande une opération de module de plateforme sécurisée qui requiert une présence physique.
ms.assetid: e71eb6ab-b6ab-4586-8999-0a464f11047a
title: Méthode SetPhysicalPresenceRequest de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 9c1b1e2760ed5015b6b682b94bd364e469edb4ed519adc371e2c348a0bf8c607
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891354"
---
# <a name="setphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Méthode SetPhysicalPresenceRequest de la \_ classe TPM Win32

La méthode **SetPhysicalPresenceRequest** de la [**classe \_ TPM Win32**](win32-tpm.md) demande une opération TPM nécessitant une présence physique. Une fois que vous avez utilisé cette méthode pour soumettre une demande, appliquez l’étape suivante indiquée dans la méthode [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md) . Enfin, utilisez la méthode [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) pour vérifier si l’opération a été exécutée avec succès. Cette méthode suspend BitLocker si l’appel de peut entraîner la nécessité d’une récupération BitLocker. BitLocker reprendra automatiquement une fois que le module de plateforme sécurisée a été approvisionné.

Ces étapes sont nécessaires, car les opérations de présence physique ne peuvent s’exécuter qu’une fois que l’ordinateur a détecté l’utilisateur physiquement présent.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetPhysicalPresenceRequest(
  [in] uint32 Request
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Demande* \[ dans\]
</dt> <dd>

Type : **UInt32**

Valeur entière qui spécifie l’opération TPM demandée qui requiert une présence physique.



| Valeur                                                                                                                               | Signification                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                                                        | Aucune demande.<br/> Utilisez cette valeur pour effacer une demande en attente.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>1</dt> </dl>                                                        | Activez le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 2.<br/> Pour plus d’informations, consultez les méthodes associées suivantes qui n’impliquent pas de présence physique : [**Enable**](enable-win32-tpm.md) et [**IsEnabled**](isenabled-win32-tpm.md).<br/>                                 |
| <dl> <dt>2</dt> </dl>                                                        | Désactivez le module TPM.<br/> Cette opération est inversée par l’opération 1.<br/> Pour plus d’informations, consultez la méthode associée qui n’implique pas de présence physique : [**Désactiver**](disable-win32-tpm.md).<br/>                                                                          |
| <dl> <dt>3</dt> </dl>                                                        | Activez le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 4.<br/>                                                                                                                                                                                                                          |
| <dl> <dt>4</dt> </dl>                                                        | Désactivez le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 3.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>5</dt> </dl>                                                        | Effacez le module de plateforme sécurisée.<br/> Cette opération ne peut pas être inversée.<br/> Pour plus d’informations, consultez la méthode associée suivante qui n’implique pas de présence physique : [**Clear**](clear-win32-tpm.md).<br/>                                                                                        |
| <dl> <dt>6</dt> </dl>                                                        | Activez et activez le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 7.<br/>                                                                                                                                                                                                               |
| <dl> <dt>7</dt> </dl>                                                        | Désactivez et désactivez le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 6.<br/>                                                                                                                                                                                                            |
| <dl> <dt>8</dt> </dl>                                                        | Autorise l’installation d’un propriétaire de module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 9.<br/>                                                                                                                                                                                                     |
| <dl> <dt>9</dt> </dl>                                                        | Empêche l’installation d’un propriétaire de module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 8. <br/>                                                                                                                                                                                                  |
| <dl> <dt>10</dt> </dl>                                                       | Activer, activer et autoriser l’installation d’un propriétaire TPM.<br/> Cette opération est inversée par l’opération 11.<br/>                                                                                                                                                                              |
| <dl> <dt>11</dt> </dl>                                                       | Désactivez, désactivez et empêchez l’installation d’un propriétaire de module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 10.<br/>                                                                                                                                                                         |
| <dl> <dt></dt><dt>12</dt> </dl> | PresenceunownedFieldUpgrade physique différé<br/> Le paramètre de présence physique a été mis à jour.<br/> **Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette valeur n’est pas prise en charge.<br/>                                                                       |
| <dl> <dt>14</dt> </dl>                                                       | Désactivez, activez et activez le module de plateforme sécurisée.<br/> Cette opération ne peut pas être inversée.<br/>                                                                                                                                                                                                               |
| <dl> <dt>15</dt> </dl>                                                       | SetNoPPIProvision \_ false<br/> Définit la configuration dont vous devez disposer physiquement pour définir le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 16.<br/> **Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette valeur n’est pas prise en charge.<br/>         |
| <dl> <dt>16</dt> </dl>                                                       | SetNoPPIProvision \_ true<br/> Définit la provision pour laquelle vous n’avez pas besoin d’être physiquement en présence pour définir le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 15.<br/> **Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette valeur n’est pas prise en charge.<br/> |
| <dl> <dt>17</dt> </dl>                                                       | SetNoPPIClear \_ false<br/> Définit la configuration dont vous devez disposer physiquement pour effacer le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 18.<br/> **Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette valeur n’est pas prise en charge.<br/>           |
| <dl> <dt>19</dt> </dl>                                                       | SetNoPPIClear \_ true<br/> Définit la provision pour laquelle vous n’avez pas besoin d’être physiquement en présence pour effacer le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 17.<br/> **Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette valeur n’est pas prise en charge.<br/>   |
| <dl> <dt>19</dt> </dl>                                                       | SetNoPPIMaintenance \_ false<br/> Définit la configuration dont vous devez disposer physiquement pour gérer le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 20.<br/> **Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette valeur n’est pas prise en charge.<br/>  |
| <dl> <dt>20</dt> </dl>                                                       | SetNoPPIMaintenance \_ true<br/> Définit la configuration pour laquelle vous n’avez pas besoin d’être physiquement en présence pour gérer le module de plateforme sécurisée.<br/> Cette opération est inversée par l’opération 19.<br/> **Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette valeur n’est pas prise en charge.<br/>   |
| <dl> <dt>21</dt> </dl>                                                       | Activer + activer + effacer<br/> Activez, activez et désactivez le module de plateforme sécurisée.<br/> **Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette valeur n’est pas prise en charge.<br/>                                                                                                  |
| <dl> <dt>22</dt> </dl>                                                       | Activer + activer + effacer + activer + activer<br/> Activez, activez et désactivez le module de plateforme sécurisée, puis activez et réactivez le module de plateforme sécurisée.<br/> **Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette valeur n’est pas prise en charge.<br/>                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.



| Code/valeur de retour                                                                                                                                                                       | Description                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | La méthode a réussi.<br/> Utilisez la méthode [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md) pour déterminer l’étape suivante nécessaire.<br/>                                                  |
| <dl> <dt>**Module TPM \_ E \_ PPP \_ non \_ pris en charge**</dt> <dt>2150171395 (0x80290303)</dt> </dl> | L’ordinateur ne prend pas en charge les opérations de présence physique TPM à l’aide de cette méthode.<br/> Pour plus d'informations, consultez le fabricant de votre ordinateur. Le BIOS de votre ordinateur peut avoir une autre prise en charge pour la configuration du module de plateforme sécurisée.<br/> |
| <dl> <dt>**Module TPM \_ \_ \_ \_ Erreur ACPI PPP**</dt> <dt>2150171392 (0x80290300)</dt> </dl>  | Une défaillance matérielle s’est produite.<br/> Pour plus d'informations, consultez le fabricant de votre ordinateur.<br/>                                                                                                                                  |



 

## <a name="remarks"></a>Remarques

Les opérations de présence physique TPM ne nécessitent pas l’autorisation du propriétaire du module de plateforme sécurisée. Toutefois, elles nécessitent des étapes supplémentaires pour aider à se protéger contre les modifications non autorisées apportées au module de plateforme sécurisée.

Les ordinateurs qui prennent en charge les opérations de présence physique TPM tenteront de détecter l’utilisateur physiquement présent avant d’exécuter l’opération. Bien que les ordinateurs puissent être différents dans la manière dont cette détection est effectuée, l’idée est d’avoir un utilisateur ou un administrateur physiquement présent autorisé à effectuer l’opération.

Par exemple, l’ordinateur peut demander à l’utilisateur de redémarrer l’ordinateur. Une fois l’ordinateur redémarré, l’ordinateur peut afficher une boîte de dialogue de confirmation du BIOS qui permet à l’utilisateur de confirmer l’opération à l’aide du clavier.

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

[**Activer**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**Désactive**](disable-win32-tpm.md)
</dt> <dt>

[**Effacer**](clear-win32-tpm.md)
</dt> </dl>

 

 
