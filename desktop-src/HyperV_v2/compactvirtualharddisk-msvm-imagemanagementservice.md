---
description: Compacte un fichier de disque dur virtuel.
ms.assetid: 1E64BD91-6FE6-4658-9EBF-615FC705B920
title: Méthode CompactVirtualHardDisk de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CompactVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e8c148e51105d8c78021b58366e2f2df3913f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521263"
---
# <a name="compactvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Méthode CompactVirtualHardDisk de la \_ classe ImageManagementService MSVM

Compacte un fichier de disque dur virtuel. Le compactage est le processus qui consiste à libérer des parties inutilisées du disque dur virtuel. Le disque dur virtuel n’est pas monté automatiquement. Consultez la section Notes pour connaître les restrictions d’utilisation de cette méthode.

## <a name="syntax"></a>Syntaxe


```mof
uint32 CompactVirtualHardDisk(
  [in]  string              Path,
  [in]  uint16              Mode,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chemin d’accès* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chemin qualifié complet qui spécifie l’emplacement du fichier de fusion.

</dd> <dt>

*Mode* \[ dans\]
</dt> <dd>

Type : **UInt16**

Spécifie le mode pour l’opération de compactage. Il doit s’agir de l’une des valeurs suivantes.

<dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

**Full** (0)


</dt> <dd></dd> <dt>

<span id="Quick"></span><span id="quick"></span><span id="QUICK"></span>

**Rapide** (1)


</dt> <dd></dd> <dt>

<span id="Retrim"></span><span id="retrim"></span><span id="RETRIM"></span>

**Retrim** (2)


</dt> <dd></dd> <dt>

<span id="Pretrimmed"></span><span id="pretrimmed"></span><span id="PRETRIMMED"></span>

**Préconformés** (3)


</dt> <dd></dd> <dt>

<span id="Prezeroed"></span><span id="prezeroed"></span><span id="PREZEROED"></span>

**Prezéros** (4)


</dt> <dd></dd> </dl> </dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Type : **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**

Référence au travail (peut avoir la **valeur null** si la tâche est terminée).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode peut retourner l’une des valeurs suivantes.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Échec** (32768)
</dt> <dt>

**Accès refusé** (32769)
</dt> <dt>

**Non pris en charge** (32770)
</dt> <dt>

**État inconnu** (32771)
</dt> <dt>

**Délai d’expiration** (32772)
</dt> <dt>

**Paramètre non valide** (32773)
</dt> <dt>

Le **système est en cours d’utilisation** (32774)
</dt> <dt>

**État non valide pour cette opération** (32775)
</dt> <dt>

**Type de données incorrect** (32776)
</dt> <dt>

Le **système n’est pas disponible** (32777)
</dt> <dt>

**Mémoire insuffisante** (32778)
</dt> <dt>

**Fichier introuvable** (32779)
</dt> </dl>

## <a name="remarks"></a>Notes

Seuls les types de disques durs virtuels suivants peuvent être utilisés avec cette méthode :

-   VHDX fixe
-   Disque dur virtuel dynamique
-   VHDX dynamique
-   Disque dur virtuel de différenciation
-   VHDX de différenciation

L’accès à la classe [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemples

L’exemple C# suivant compacte un disque dur virtuel. Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).


```CSharp
public enum VirtualHardDiskCompactMode
{
    Full = 0,
    Quick = 1,
    Retrim = 2,
    Pretrimmed = 3,
    Prezeroed = 4
}

public static void CompactVirtualHardDisk(string vhdPath, VirtualHardDiskCompactMode compactMode)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("CompactVirtualHardDisk");
    inParams["Path"] = vhdPath;
    inParams["Mode"] = compactMode;
    ManagementBaseObject outParams = imageService.InvokeMethod("CompactVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was compacted successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to compact {0}", inParams["Path"]);
        }
    }
    else
    {
        Console.WriteLine("Compact {0} returned error {1}", inParams["Path"], outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

