---
title: Énumération DeliveryOptimizationFileProperty (Deliveryoptimization. h)
description: L’énumération DeliveryOptimizationFileProperty spécifie l’ID d’une propriété facultative pour le fichier d’optimisation de la remise.
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
ms.openlocfilehash: 7c670118a66525c2a890a8c1ed96e4eefb5f5c28
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520251"
---
# <a name="deliveryoptimizationfileproperty-enumeration"></a>Énumération DeliveryOptimizationFileProperty

L’énumération DeliveryOptimizationFileProperty spécifie l’ID d’une propriété facultative pour le fichier d’optimisation de la remise. Cette énumération est utilisée dans l’interface IDeliveryOptimizationFile2 où la valeur de propriété de type VARIANT est passée

## <a name="syntax"></a>Syntax

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

L’ID de propriété DOFilePropertyId_IntegrityCheckInfo définit l’emplacement du fichier de hachage de la pièce (PHF), qui est utilisé par l’optimisation de la distribution pour effectuer des vérifications de l’intégrité du Runtime sur le contenu téléchargé. DOFilePropertyId_IntegrityCheckInfo est une propriété en écriture seule de type VT_BSTR.

</dd> <dt>

DOFilePropertyId_IntegrityCheckMandatory
</dt> <dd>

L’ID de propriété DOFilePropertyId_IntegrityCheckMandatory définit un indicateur booléen indiquant si l’utilisation du PHF est obligatoire. Si la valeur est TRUE, le téléchargement est abandonné après l’échec de la vérification de l’intégrité. DOFilePropertyId_IntegrityCheckMandatory est une propriété en lecture/écriture de type VT_BOOL.

</dd> <dt>

DOFilePropertyId_DownloadSinkFilePath
</dt> <dd>

L’ID de propriété DOFilePropertyId_DownloadSinkFilePath définit un emplacement de système de fichiers complet où l’optimisation de la distribution doit stocker les éléments téléchargés. DOFilePropertyId_DownloadSinkFilePath est de type VT_BSTR.

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
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1803 \[ uniquement\]<br/>      |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>  |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>               |
