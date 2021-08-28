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
ms.openlocfilehash: d91ff44e3b4f4247983ec81d53257347c8bcfa523f85855dcd0d37074f4b38fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498949"
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
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |