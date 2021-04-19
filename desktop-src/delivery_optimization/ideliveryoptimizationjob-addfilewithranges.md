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
ms.openlocfilehash: cc147f5cb3f91a2fe0b8518493dba72798ce8056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510367"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs de retour suivantes, ainsi que d’autres.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Code de retour</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong><strong>S_OK</strong></strong></dt> </dl></td>
<td>Opération réussie.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> </dl></td>
<td>Le nom de fichier local est NULL ou une chaîne vide. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>E_ACCESSDENIED</strong></dt> </dl></td>
<td>L’utilisateur n’a pas l’autorisation d’écrire dans le répertoire spécifié sur le client.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>DO_E_INVALID_RANGE</strong></dt> </dl></td>
<td>L’une des plages n’est pas valide. Par exemple, InitialOffset est défini sur <strong>BG_LENGTH_TO_EOF</strong>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </dl></td>
<td>Vous ne pouvez pas spécifier des plages en double ou qui se chevauchent. <br/>
<blockquote>
[!Note]<br />
Les plages sont triées selon le décalage de la valeur, et non la longueur. Si des plages ont le même décalage, mais sont dans l’ordre inverse, cette erreur est retournée. Par exemple, si 100,5 et 100,0 sont entrés dans cet ordre, vous ne serez pas en mesure d’ajouter le fichier au travail.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>DO_E_INVALID_STATE</strong></dt> </dl></td>
<td>L’état du travail ne peut pas être <strong>BG_JOB_STATE_CANCELLED</strong> ou <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob est défini comme EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDeliveryOptimizationJob**](ideliveryoptimizationjob.md)
</dt> </dl>

 

