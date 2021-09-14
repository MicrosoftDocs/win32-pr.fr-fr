---
description: Représente le Module de plateforme sécurisée (TPM) (TPM), une puce de sécurité matérielle qui fournit une racine de confiance pour un système informatique.
ms.assetid: da4ba366-49af-420e-a2ad-80bba34b3b00
title: Classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm
- Win32_Tpm.IsActivated_InitialValue
- Win32_Tpm.IsEnabled_InitialValue
- Win32_Tpm.IsOwned_InitialValue
- Win32_Tpm.SpecVersion
- Win32_Tpm.ManufacturerVersion
- Win32_Tpm.ManufacturerVersionInfo
- Win32_Tpm.ManufacturerId
- Win32_Tpm.PhysicalPresenceVersionInfo
api_type:
- DllExport
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d8d6eac9fba875484ba2f08e149608c9994a1087
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013584"
---
# <a name="win32_tpm-class"></a>\_Classe TPM Win32

La **classe \_ TPM Win32** représente le module de plateforme sécurisée (TPM) (TPM), une puce de sécurité matérielle qui fournit une racine de confiance pour un système informatique.

## <a name="syntax"></a>Syntaxe

``` syntax
class Win32_Tpm
{
  boolean IsActivated_InitialValue;
  boolean IsEnabled_InitialValue;
  boolean IsOwned_InitialValue;
  string  SpecVersion;
  string  ManufacturerVersion;
  string  ManufacturerVersionInfo;
  uint32  ManufacturerId;
  string  PhysicalPresenceVersionInfo;
};
```

## <a name="members"></a>Membres

La **classe \_ TPM Win32** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La **classe \_ TPM Win32** possède ces méthodes.



| Méthode                                                                                   | Description                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBlockedCommand**](addblockedcommand-win32-tpm.md)                                 | Ajoute une commande TPM à la liste locale des commandes bloquées sur Windows.<br/>                                                                                                             |
| [**ChangeOwnerAuth**](changeownerauth-win32-tpm.md)                                     | Modifie la valeur d’autorisation du propriétaire du module de plateforme sécurisée.<br/>                                                                                                                                       |
| [**Effacé**](clear-win32-tpm.md)                                                         | Réinitialise le module de plateforme sécurisée à son état d’usine par défaut.<br/>                                                                                                                                     |
| [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md)                               | Convertit une phrase secrète fournie par l’utilisateur en une valeur d’autorisation de propriétaire de 20 octets qui peut être utilisée pour interagir avec le module de plateforme sécurisée.<br/>                                                            |
| [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)                   | Crée une paire de clés de type EK 2048 bits sur le module de plateforme sécurisée.<br/>                                                                                                                              |
| [**Désactiver**](disable-win32-tpm.md)                                                     | Autorise le propriétaire du module de plateforme sécurisée à désactiver le module de plateforme sécurisée.<br/>                                                                                                                                         |
| [**Rendre**](enable-win32-tpm.md)                                                       | Autorise le propriétaire du module de plateforme sécurisée à activer le module de plateforme sécurisée.<br/>                                                                                                                                          |
| [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md)               | Obtient et retourne l’opération de présence physique TPM en attente. Utilisez la méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) pour demander une opération.<br/> |
| [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md)             | Obtient et retourne les résultats d’une opération de présence physique TPM effectuée.<br/>                                                                                          |
| [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)         | Indique l’action de l’utilisateur nécessaire pour effectuer une opération de présence physique TPM.<br/>                                                                                           |
| [**IsActivated**](isactivated-win32-tpm.md)                                             | Indique si le module de plateforme sécurisée est activé.<br/>                                                                                                                                          |
| [**IsCommandBlocked**](iscommandblocked-win32-tpm.md)                                   | Indique si la commande TPM peut s’exécuter sur ce système d’exploitation.<br/>                                                                                                              |
| [**IsCommandPresent**](iscommandpresent-win32-tpm.md)                                   | Indique si une commande de module de plateforme sécurisée est prise en charge par cet ordinateur.<br/>                                                                                                                   |
| [**IsEnabled**](isenabled-win32-tpm.md)                                                 | Indique si le module de plateforme sécurisée est activé.<br/>                                                                                                                                            |
| [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md)             | Indique si le module de plateforme sécurisée a une paire de clés de type EK.<br/>                                                                                                                           |
| [**IsOwned**](isowned-win32-tpm.md)                                                     | Indique si le module de plateforme sécurisée a un propriétaire.<br/>                                                                                                                                          |
| [**IsOwnerClearDisabled**](isownercleardisabled-win32-tpm.md)                           | Indique si le propriétaire du module de plateforme sécurisée peut effacer le module de plateforme sécurisée.<br/>                                                                                                                               |
| [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md)                               | Indique si un propriétaire de module de plateforme sécurisée peut être installé.<br/>                                                                                                                                  |
| [**IsPhysicalClearDisabled**](isphysicalcleardisabled-win32-tpm.md)                     | Indique si une opération de présence physique TPM peut effacer le module de plateforme sécurisée.<br/>                                                                                                           |
| [**IsPhysicalPresenceHardwareEnabled**](isphysicalpresencehardwareenabled-win32-tpm.md) | Indique si cet ordinateur prend en charge un chemin d’accès matériel dédié pour signaler la présence physique.<br/>                                                                                  |
| [**IsSrkAuthCompatible**](issrkauthcompatible-win32-tpm.md)                             | indique si l’autorisation de clé racine Stockage est compatible avec Windows.<br/>                                                                                           |
| [**RemoveBlockedCommand**](removeblockedcommand-win32-tpm.md)                           | Supprime une commande TPM de la liste locale des commandes bloquées par Windows.<br/>                                                                                                        |
| [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md)                                   | Réinitialise le délai d’attente ou tout autre mécanisme que les fabricants de module de plateforme sécurisée implémentent pour se protéger contre les attaques par dictionnaire sur le module de plateforme sécurisée.<br/>                                                 |
| [**ResetSrkAuth**](resetsrkauth-win32-tpm.md)                                           | réinitialise la valeur d’autorisation de la clé racine de Stockage (SRK) pour qu’elle soit compatible avec Windows.<br/>                                                                                             |
| [**SelfTest**](selftest-win32-tpm.md)                                                   | Effectue un test automatique du module de plateforme sécurisée et retourne le résultat.<br/>                                                                                                                          |
| [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)               | Demande l’exécution d’une opération de présence physique TPM.<br/>                                                                                                                               |
| [**TakeOwnership**](takeownership-win32-tpm.md)                                         | Installe un propriétaire pour le module de plateforme sécurisée.<br/>                                                                                                                                                   |



 

### <a name="properties"></a>Propriétés

La **classe \_ TPM Win32** possède ces propriétés.

<dl> <dt>

**IsActivated \_ InitialValue**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le module de plateforme sécurisée est activé.

**true** si l’appareil est activé (autrement dit, si **isActivated \_ InitialValue** a la valeur true); sinon, **false**.

Cette valeur est stockée lorsque la classe est instanciée. Il est possible que le module de plateforme sécurisée change d’État entre l’instanciation et lorsque vous vérifiez cette valeur. Pour vérifier si le module de plateforme sécurisée est activé en temps réel, utilisez la méthode [**isActivated**](isactivated-win32-tpm.md) .

**Windows Server 2008 et Windows Vista :** Cette propriété n’est pas disponible.

</dd> <dt>

**IsEnabled \_ InitialValue**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le module de plateforme sécurisée est activé.

**true** si l’appareil est activé (autrement dit, si **IsEnabled \_ InitialValue** a la valeur true); sinon, **false**.

Cette valeur est stockée lorsque la classe est instanciée. Il est possible que le module de plateforme sécurisée change d’État entre l’instanciation et lorsque vous vérifiez cette valeur. Pour vérifier si le module de plateforme sécurisée est activé en temps réel, utilisez la méthode [**IsEnabled**](isenabled-win32-tpm.md) .

**Windows Server 2008 et Windows Vista :** Cette propriété n’est pas disponible.

</dd> <dt>

**IsOwned \_ InitialValue**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le module de plateforme sécurisée a un propriétaire.

**true** si l’appareil a un propriétaire (autrement dit, si **IsOwned \_ InitialValue** a la valeur true); sinon, **false**.

Cette valeur est stockée lorsque la classe est instanciée. Il est possible que le module de plateforme sécurisée change d’État entre l’instanciation et lorsque vous vérifiez cette valeur. Pour vérifier si le module de plateforme sécurisée est détenu en temps réel, utilisez la méthode [**IsOwned**](isowned-win32-tpm.md) .

**Windows Server 2008 et Windows Vista :** Cette propriété n’est pas disponible.

</dd> <dt>

**ManufacturerId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Informations d’identification qui renomment de façon unique le fabricant du module de plateforme sécurisée.

Lorsque les données ne sont pas disponibles, la valeur zéro est retournée.

Cette valeur entière peut être convertie en valeur de chaîne en interprétant chaque octet comme un caractère ASCII. Par exemple, une valeur entière de 1414548736 peut être divisée en ces 4 octets : 0x54, 0x50, 0x4D et 0x00. En supposant que la chaîne est interprétée de gauche à droite, cette valeur entière est convertie en valeur de chaîne « TPM ».

</dd> <dt>

**ManufacturerVersion**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Version du module de plateforme sécurisée (TPM), telle que spécifiée par le fabricant.

Lorsque les données ne sont pas disponibles, « non pris en charge » est retourné.

</dd> <dt>

**ManufacturerVersionInfo**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Autres informations de version spécifiques au fabricant pour le module de plateforme sécurisée.

Lorsque les données ne sont pas disponibles, « non pris en charge » est retourné.

</dd> <dt>

**PhysicalPresenceVersionInfo**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

La version de l’interface de présence physique, un mécanisme de communication utilisé pour exécuter des opérations d’appareil qui nécessitent une présence physique, que l’ordinateur prend en charge.

Cette interface doit être disponible pour exécuter des opérations de présence physique TPM. Les **méthodes \_ TPM Win32** [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)et [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) exposent les fonctionnalités de l’interface de présence physique.

Lorsque les données ne sont pas disponibles, « non pris en charge » est retourné.

</dd> <dt>

**SpecVersion**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Version de la spécification du Trusted Computing Group (TCG) que le module de plateforme sécurisée prend en charge. Cette valeur comprend la version principale et secondaire de la spécification TCG, le niveau de révision de la spécification et le niveau de révision de l’errata. Toutes les valeurs sont au format hexadécimal. Par exemple, les informations de version « 1,2, 2, 0 » indiquent que l’appareil a été implémenté à la spécification TCG version 1,2, version de révision 2 et sans errata.

Lorsque les données ne sont pas disponibles, « non pris en charge » est retourné.

</dd> </dl>

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



 

 
