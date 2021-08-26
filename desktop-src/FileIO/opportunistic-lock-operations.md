---
description: Si une application demande des verrous opportunistes, tous les fichiers pour lesquels elle demande des verrous doivent être ouverts pour les entrées et sorties avec chevauchement (asynchrone) à l’aide de la fonction CreateFile avec l’indicateur de CHEVAUCHement de l’indicateur de fichier \_ \_ .
ms.assetid: 1595c03e-9f6d-456c-8164-fafba06bbd79
title: Opérations de verrouillage opportuniste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fc24c0b503ec23d20be414508371c5e1f63e93d3b009a42e84d742e5f014c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927639"
---
# <a name="opportunistic-lock-operations"></a>Opérations de verrouillage opportuniste

Si une application demande des verrous opportunistes, tous les fichiers pour lesquels elle demande des verrous doivent être ouverts pour les entrées et sorties avec chevauchement (asynchrone) à l’aide de la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) avec l’indicateur de **\_ \_ chevauchement** de l’indicateur de fichier. Une fois les fichiers ouverts pour une opération avec chevauchement, vous pouvez utiliser la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec l’un des codes de contrôle suivants pour travailler avec ces fichiers «verrous opportunistes :

<dl>

[**fermeture de l’accusé de réception FSCTL \_ OPBATCH \_ \_ \_ en attente**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**FSCTL de \_ rupture de verrou OPLOCK \_ \_ \_ non \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**\_accusé de réception FSCTL OPLOCK \_ break \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**\_notification de \_ rupture \_ OPLOCK FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**\_ \_ OPLOCK batch de demande FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**\_ \_ OPLOCK filtre de requête FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**\_OPLOCK Request \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**FSCTL \_ demande \_ OPLOCK \_ niveau \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**FSCTL \_ demande \_ OPLOCK \_ niveau \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 
