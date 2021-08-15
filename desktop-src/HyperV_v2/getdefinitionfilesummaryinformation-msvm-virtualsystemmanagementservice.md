---
description: Retourne les informations de résumé de l’ordinateur virtuel pour les fichiers de définition d’ordinateur virtuel spécifiés.
ms.assetid: 5a3d7f2c-3b89-4dd6-909d-4452afc3705f
title: Méthode GetDefinitionFileSummaryInformation de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetDefinitionFileSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7c6d3da6ef920488edb7fde723880b9f53768cfd246e91d287390bb6fb02fb17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995296"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode GetDefinitionFileSummaryInformation de la \_ classe VirtualSystemManagementService MSVM

Retourne les informations de résumé de l’ordinateur virtuel pour les fichiers de définition d’ordinateur virtuel spécifiés.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DefinitionFiles* \[ dans\]
</dt> <dd>

Tableau de chemins d’accès aux fichiers de configuration XML pour lesquels retourner les informations de résumé.

</dd> <dt>

*SummaryInformation* \[ à\]
</dt> <dd>

Tableau d’instances [**de \_ SummaryInformationBase MSVM**](msvm-summaryinformation.md) contenant les informations demandées pour les ordinateurs virtuels et/ou les instantanés spécifiés dans le tableau *DefinitionFiles* . Seules les propriétés **Name**, **ElementName**, **CreationTime** et **Notes** sont retournées, toutes les autres propriétés ont la **valeur null**.

> [!Note]  

 

avant Windows 10, la version 1703, datatype était [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md).

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
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




