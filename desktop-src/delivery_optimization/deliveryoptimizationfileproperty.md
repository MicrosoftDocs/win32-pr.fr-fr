---
title: Énumération DeliveryOptimizationFileProperty (Deliveryoptimization. h)
description: L’énumération DeliveryOptimizationFileProperty spécifie l’ID d’une propriété facultative pour le fichier DO.
keywords:
- Énumération DeliveryOptimizationFileProperty
topic_type:
- apiref
api_name:
- DeliveryOptimizationFileProperty
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 238ad815149f7d40dd1902b991608e0a3005eb35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543624"
---
# <a name="deliveryoptimizationfileproperty-enumeration"></a>Énumération DeliveryOptimizationFileProperty

L’énumération DeliveryOptimizationFileProperty spécifie l’ID d’une propriété facultative pour le fichier DO. Cette énumération est utilisée dans l’interface IDeliveryOptimizationFile2 où la valeur de propriété de type VARIANT est passée

## <a name="syntax"></a>Syntaxe

```C++
typedef enum _DeliveryOptimizationFileProperty {  
  DOFilePropertyId_DecryptionInfo,
  DOFilePropertyId_IntegrityCheckInfo,
  DOFilePropertyId_IntegrityCheckMandatory,
  DOFilePropertyId_DownloadSinkInterface,
  DOFilePropertyId_DownloadSinkFilePath,
  DOFilePropertyId_DownloadSinkMemoryStream,
  DOFilePropertyId_TotalSizeBytes
} DOFilePropertyId;
```

## <a name="constants"></a>Constantes

<dl> <dt>

DOFilePropertyId_DecryptionInfo
</dt> <dd>

L’ID de propriété DOFilePropertyId_DecryptionInfo définit les informations de déchiffrement sous la forme d’une chaîne JSON. DOFilePropertyId_DecryptionInfo est une propriété en écriture seule de type VT_BSTR.

</dd> <dt>

DOFilePropertyId_IntegrityCheckInfo
</dt> <dd>

L’ID de propriété DOFilePropertyId_IntegrityCheckInfo définit l’emplacement du fichier de hachage de la pièce (PHF), qui est utilisé par pour effectuer des vérifications de l’intégrité du Runtime sur le contenu téléchargé. DOFilePropertyId_IntegrityCheckInfo est une propriété en écriture seule de type VT_BSTR.

</dd> <dt>

DOFilePropertyId_IntegrityCheckMandatory
</dt> <dd>

L’ID de propriété DOFilePropertyId_IntegrityCheckMandatory définit un indicateur booléen indiquant si l’utilisation du PHF est obligatoire. Si la valeur est TRUE, le téléchargement est abandonné après l’échec de la vérification de l’intégrité. DOFilePropertyId_IntegrityCheckMandatory est une propriété en lecture/écriture de type VT_BOOL.

</dd> <dt>

DOFilePropertyId_DownloadSinkFilePath
</dt> <dd>

L’ID de propriété DOFilePropertyId_DownloadSinkFilePath définit un emplacement de système de fichiers complet où doit stocker les éléments téléchargés. DOFilePropertyId_DownloadSinkFilePath est de type VT_BSTR.

</dd> <dt>

DOFilePropertyId_DownloadSinkMemoryStream
</dt> <dd>

L’ID de propriété DOFilePropertyId_DownloadSinkMemoryStream est déconseillé. Ne pas utiliser.

</dd> <dt>

DOFilePropertyId_TotalSizeBytes
</dt> <dd>

L’ID de propriété DOFilePropertyId_TotalSizeBytes spécifie la taille totale du téléchargement. DOFilePropertyId_TotalSizeBytes est de type VT_UI8.
</dd> </dl>

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------|----------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1803 \[ uniquement\]<br/>      |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>  |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>               |
