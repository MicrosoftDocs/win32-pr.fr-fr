---
title: Classe MDM_RemoteWipe
description: La \_ classe MDM RemoteWipe permet la réinitialisation à distance d’un appareil.
ms.assetid: 8c7c8705-8694-4ce3-ba21-ca610fe1f547
keywords:
- Classe MDM_RemoteWipe
- Classe MDM_RemoteWipe, Description
topic_type:
- apiref
api_name:
- MDM_RemoteWipe
- MDM_RemoteWipe.InstanceID
- MDM_RemoteWipe.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ca943ed0b226f9006733b3e9d8745172cfe9e08
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520056"
---
# <a name="mdm_remotewipe-class"></a>\_Classe REMOTEWIPE MDM

> [!NOTE]
> **Certaines informations portent sur la préversion du produit, qui est susceptible d’être en grande partie modifié avant sa commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.**

La classe **MDM \_ RemoteWipe** permet la réinitialisation à distance d’un appareil.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_RemoteWipe
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a>Membres

La **classe \_ RemoteWipe MDM** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MDM \_ RemoteWipe** possède ces méthodes.

| Méthode                                              | Description                                              |
|:----------------------------------------------------|:---------------------------------------------------------|
| [**doWipeMethod**](mdm-remotewipe-dowipemethod.md) | Déclenche le démarrage de la réinitialisation à distance par l’appareil. |
| [**doWipePersistProvisionedDataMethod**](mdm-remotewipe-dowipepersistprovisioneddatamethod.md) | Déclenche l’appareil pour sauvegarder les données de configuration dans un emplacement persistant et effectuer une réinitialisation à distance sur l’appareil. Les informations qui ont été sauvegardées seront restaurées et appliquées à l’appareil lors de la reprise. |
| [**doWipePersistUserDataMethod**](mdm-remotewipe-dowipepersistuserdatamethod.md) | Déclenche l’appareil pour démarrer la réinitialisation à distance tout en conservant les comptes d’utilisateur et les données. |
| [**doWipeProtectedMethod**](mdm-remotewipe-dowipeprotectedmethod.md) | Déclenche l’appareil pour démarrer la réinitialisation à distance sur l’appareil et nettoyer entièrement le lecteur interne. Dans certaines configurations d’appareil, cette commande risque de ne pas pouvoir démarrer l’appareil. |

### <a name="properties"></a>Propriétés

La **classe \_ RemoteWipe MDM** a ces propriétés.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifie le nom du nœud parent. Pour cette classe, la chaîne est « RemoteWipe ».

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/ »

</dd> </dl>

## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser RemoteWipe et appeler doWipeMethod.

> [!Note]  
> Cet exemple doit être exécuté sous utilisateur du système local. Pour ce faire, téléchargez l’outil PsExec depuis <https://technet.microsoft.com/sysinternals/bb897553.aspx> et exécutez `psexec.exe -i -s cmd.exe` à partir d’une invite de commandes d’administrateur élevé.

``` syntax
$namespaceName = "root\cimv2\mdm\dmmap"
$className = "MDM_RemoteWipe"
$methodName = "doWipeMethod"

$session = New-CimSession

$params = New-Object Microsoft.Management.Infrastructure.CimMethodParametersCollection
$param = [Microsoft.Management.Infrastructure.CimMethodParameter]::Create("param", "", "String", "In")
$params.Add($param)

try
{
    $instance = Get-CimInstance -Namespace $namespaceName -ClassName $className -Filter "ParentID='./Vendor/MSFT' and InstanceID='RemoteWipe'"
    $session.InvokeMethod($namespaceName, $instance, $methodName, $params)
}
catch [Exception]
{
    write-host $_ | out-string
}
```

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows 10 \[ applications de bureau uniquement\]                                                    |
| Serveur minimal pris en charge | Aucun pris en charge                                                                      |
| Espace de noms                | Racine DMMap de gestion des appareils mobiles \\ \\ \\                                                             |
| MOF                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>
