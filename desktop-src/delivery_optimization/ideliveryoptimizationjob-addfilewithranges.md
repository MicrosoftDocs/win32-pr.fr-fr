---
title: Méthode IDeliveryOptimizationJob AddFileWithRanges (Deliveryoptimization. h)
description: Ajoute un fichier à un travail de téléchargement et spécifie les plages du fichier que vous souhaitez télécharger.
ms.assetid: 23F0A39F-670F-4030-A3B3-4F9277FFA8AB
keywords:
- Méthode AddFileWithRanges
- Méthode AddFileWithRanges, interface IDeliveryOptimizationJob
- Interface IDeliveryOptimizationJob, méthode AddFileWithRanges
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob.AddFileWithRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 197aa7443123c81d1a675d321b91573823a84f15
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476126"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a>IDeliveryOptimizationJob :: AddFileWithRanges, méthode

Ajoute un fichier à un travail de téléchargement et spécifie les plages du fichier que vous souhaitez télécharger.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddFileWithRanges(
  [in]           LPCWSTR       fileId,
  [in]           LPCWSTR       remoteUrl,
  [in]           LPCWSTR       localName,
  [in, optional] DWORD         rangeCount,
  [in, optional] BG_FILE_RANGE ranges[],
  [in, optional] ULONG64       fileSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fileid* \[ dans\]
</dt> <dd>

Chaîne terminée par le caractère null qui est un identificateur unique du contenu publié. Pour du contenu non publié, il peut s’agir d’une chaîne unique que l’appelant peut utiliser pour identifier des fichiers dans un travail.

</dd> <dt>

*remoteUrl* \[ dans\]
</dt> <dd>

Chaîne terminée par le caractère null qui contient le nom du fichier sur le serveur.

</dd> <dt>

*LocalName* \[ dans\]
</dt> <dd>

Chaîne terminée par le caractère null qui contient le nom du fichier sur le client.

</dd> <dt>

*rangeCount* \[ dans, facultatif\]
</dt> <dd>

Nombre d’éléments dans les *plages*.

</dd> <dt>

*plages* \[ dans, facultatif\]
</dt> <dd>

Tableau d’une ou de plusieurs structures de [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) qui spécifient les plages à télécharger. Ne spécifiez pas de doublons ou de plages qui se chevauchent.

</dd> <dt>

*taille* \[ du dans, facultatif\]
</dt> <dd>

Taille du fichier en octets. Transmettez **DO_UNKNOWN_FILE_SIZE** si la taille n’est pas connue de l’application de l’appelant.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne les valeurs de retour suivantes, ainsi que d’autres.




| Code de retour | Description | 
|-------------|-------------|
| <dl><dt><strong><strong>S_OK</strong></strong></dt></dl> | Réussite.<br /> | 
| <dl><dt><strong>E_INVALIDARG</strong></dt></dl> | Le nom de fichier local est NULL ou une chaîne vide. <br /> | 
| <dl><dt><strong>E_ACCESSDENIED</strong></dt></dl> | L’utilisateur n’a pas l’autorisation d’écrire dans le répertoire spécifié sur le client.<br /> | 
| <dl><dt><strong>DO_E_INVALID_RANGE</strong></dt></dl> | L’une des plages n’est pas valide. Par exemple, InitialOffset est défini sur <strong>BG_LENGTH_TO_EOF</strong>.<br /> | 
| <dl><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt></dl> | Vous ne pouvez pas spécifier des plages en double ou qui se chevauchent. <br /><blockquote>[!Note]<br />Les plages sont triées selon le décalage de la valeur, et non la longueur. Si des plages ont le même décalage, mais sont dans l’ordre inverse, cette erreur est retournée. Par exemple, si 100,5 et 100,0 sont entrés dans cet ordre, vous ne serez pas en mesure d’ajouter le fichier au travail.</blockquote><br /> | 
| <dl><dt><strong>DO_E_INVALID_STATE</strong></dt></dl> | L’état du travail ne peut pas être <strong>BG_JOB_STATE_CANCELLED</strong> ou <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.<br /> | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob est défini comme EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDeliveryOptimizationJob**](ideliveryoptimizationjob.md)
</dt> </dl>

 

