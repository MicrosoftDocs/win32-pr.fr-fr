---
description: Exporte une collection de points de référence dans un fichier. La collection de points de référence, ses paramètres de configuration associés et les paramètres de ressources qui lui sont associés sont conservés dans le fichier résultant.
ms.assetid: 0ed61ded-b4d6-40c5-98be-e192eb934387
title: Méthode ExportReferencePoint de la classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3084cdecdd9a5c5808884a609b6bd91f4d50b814d64a96c8ea9e7470c9ece728
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681899"
---
# <a name="exportreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>Méthode ExportReferencePoint de la \_ classe CollectionReferencePointService MSVM

Exporte une collection de points de référence dans un fichier. La collection de points de référence, ses paramètres de configuration associés et les paramètres de ressources qui lui sont associés sont conservés dans le fichier résultant.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ExportReferencePoint(
  [in]  CIM_Collection  REF ReferencePointCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ReferencePointCollection* \[ dans\]
</dt> <dd>

Référence à une [**\_ collection CIM**](cim-collection.md) qui représente la collection de points de référence à exporter.

</dd> <dt>

*ExportDirectory* \[ dans\]
</dt> <dd>

Chemin d’accès complet du répertoire dans lequel la collection de points de référence doit être exportée.

</dd> <dt>

*ExportSettingData* \[ dans\]
</dt> <dd>

Instance de [**MSVM \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) qui représente les paramètres de l’opération d’exportation.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Référence facultative qui est retournée si l’opération est exécutée de façon asynchrone. Si elle est présente, la référence retournée à une instance de [**\_ ConcreteJob CIM**](cim-concretejob.md) peut être utilisée pour surveiller la progression et pour obtenir le résultat de la méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est exécutée de façon synchrone, elle retourne 0 si elle réussit. Si cette méthode est exécutée de façon asynchrone, elle retourne 4096 et le paramètre de sortie de la tâche peut être utilisé pour suivre la progression de l’opération asynchrone. Toute autre valeur de retour indique une erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




