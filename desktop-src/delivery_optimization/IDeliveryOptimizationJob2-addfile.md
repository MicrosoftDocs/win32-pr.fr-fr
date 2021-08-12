---
title: Méthode IDeliveryOptimizationJob2 AddFile
description: La méthode AddFile ajoute un seul fichier à une tâche DO existante.
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
ms.openlocfilehash: e6d27bca855bb9c719b485060fabf1f10b7130bd864569e74f98516ca76b8fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544634"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a>IDeliveryOptimizationJob2 :: AddFileWithRanges, méthode

La méthode AddFile ajoute un seul fichier à une tâche DO existante.

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

L’URL de fichier qui tentera de se connecter pour télécharger le fichier.

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

## <a name="return-value"></a>Valeur retournée

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
