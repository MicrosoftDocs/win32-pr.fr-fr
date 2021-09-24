---
title: Méthode IDeliveryOptimizationJob2 AddFile
description: La méthode AddFile ajoute un seul fichier à une tâche d’optimisation de la remise existante.
keywords:
- AddFile (méthode)
- Méthode AddFile, interface IDeliveryOptimizationJob2
- Interface IDeliveryOptimizationJob2, méthode AddFile
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.AddFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 217215d6f4aaf96de8deab37d08cc492392c0631
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128519891"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a>IDeliveryOptimizationJob2 :: AddFileWithRanges, méthode

La méthode AddFile ajoute un seul fichier à une tâche d’optimisation de la remise existante.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT AddFile(
  [in]                              LPCWSTR       fileId,
  [in, unique]                      LPCWSTR       remoteUrl,
  [in]                              DWORD         rangeCount,
  [in, size_is(rangeCount), unique] BG_FILE_RANGE ranges[],
  [in]                              REFIID        riid,
  [out]                             void          **object
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*fileid* \[ dans\]
</dt> <dd>

La chaîne d’ID de fichier, qui identifie de façon unique le fichier à télécharger.

</dd> <dt>

*remoteUrl* \[ dans\]
</dt> <dd>

URL de fichier que l’optimisation de la distribution tentera de se connecter pour télécharger le fichier.

</dd> <dt>

*rangeCount* \[ dans\]
</dt> <dd>

Nombre d’éléments contenus dans les *plages*. Une valeur zéro signifie qu’aucune plage n’est utilisée pour le fichier.

</dd> <dt>

*plages* \[ dans\]
</dt> <dd>

Liste de plages facultatives. Chaque plage de la liste est une structure [**BG_FILE_RANGE**](bg-file-range.md) .

</dd> <dt>

*riid* \[ dans\]
</dt> <dd>

Type de l’objet contenu dans l’objet. Le type doit être IID_IDeliveryOptimizationFile.

</dd> <dt>

*objet* \[ à\]
</dt> <dd>

Objet IDeliveryOptimizationFile, qui représente le fichier de téléchargement. 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne S_OK en cas de réussite ou une des valeurs HRESULT standard en cas d’erreur.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|---------------------------|---------------------------------------------------------------------------------|
| Client minimal pris en charge  | Windows 10, les applications de bureau version 1803 \[ uniquement\]                                  |
| Serveur minimal pris en charge  | Windows Serveur, version 1709 \[ applications de bureau uniquement\]                              |
| En-tête                    | Deliveryoptimization. h                                                          |
| MIDL                       | DeliveryOptimization. idl                                                        |
| Bibliothèque                   | Dosvc. lib                                                                       |
| DLL                       | Dosvc.dll                                                                       |
| IID                       | IID_IDeliveryOptimizationJob est défini comme EE2584CF-A69C-4848-B633-2649962B3EF7 |

## <a name="see-also"></a>Voir aussi

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
