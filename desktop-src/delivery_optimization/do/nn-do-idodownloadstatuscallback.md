---
title: Interface IDODownloadStatusCallback
description: Utilisé pour recevoir des notifications relatives à un téléchargement.
keywords:
- Interface IDODownloadStatusCallback
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0917b73939535854469a1fe02ea89acc904cf055
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382009"
---
# <a name="idodownloadstatuscallback-interface"></a>Interface IDODownloadStatusCallback

L’interface **IDODownloadStatusCallback** est utilisée pour recevoir des notifications relatives à un téléchargement.

## <a name="methods"></a>Méthodes

L’interface **IDODownloadStatusCallback** possède ces méthodes.

| Méthode | Description |
| ---- |:---- |
| [IDODownloadStatusCallback::OnStatusChanged](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | Appelle votre implémentation de cette méthode chaque fois qu’un état de téléchargement a changé. |

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Server, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |