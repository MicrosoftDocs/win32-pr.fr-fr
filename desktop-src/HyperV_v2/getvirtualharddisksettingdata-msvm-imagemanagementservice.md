---
description: Récupère les données de paramètre associées à un fichier de disque dur virtuel.
ms.assetid: b82c018e-8d23-4615-99c1-3b622a8f41da
title: Méthode GetVirtualHardDiskSettingData de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualHardDiskSettingData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: cf8f19d3bbdac593dabef0a1ff8e9c9b60027301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950997"
---
# <a name="getvirtualharddisksettingdata-method-of-the-msvm_imagemanagementservice-class"></a>Méthode GetVirtualHardDiskSettingData de la \_ classe ImageManagementService MSVM

Récupère les données de paramètre associées à un fichier de disque dur virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetVirtualHardDiskSettingData(
  [in]  string              Path,
  [out] string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chemin d’accès* \[ dans\]
</dt> <dd>

Chemin d’accès complet du fichier image de disque.

</dd> <dt>

*SettingData* \[ à\]
</dt> <dd>

En cas de réussite, reçoit une instance incorporée de la classe [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) qui contient les données de paramètre pour le disque dur virtuel.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

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

L’accès à la classe [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemples

L’exemple C# suivant montre comment appeler la méthode [**GetVirtualHardDiskState**](getvirtualharddiskstate-msvm-imagemanagementservice.md) . Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).


```CSharp
public static void GetVirtualHardDiskSettingData(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");
    ManagementBaseObject inParams = imageService.GetMethodParameters("GetVirtualHardDiskSettingData");

    inParams["Path"] = vhdPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("GetVirtualHardDiskSettingData", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("GetVirtualHardDiskSettingData was successful.");
        }
        else
        {
            Console.WriteLine("GetVirtualHardDiskSettingData was not successful.");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        string diskStateString = outParams["SettingData"].ToString();
        Utility.PrintEmbeddedInstance(diskStateString);
    }

    outParams.Dispose();
    inParams.Dispose();
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

[**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

