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
ms.openlocfilehash: a6db896bf8d70e795b16512d22027c7ab6a02e91
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521336"
---
# <a name="idodownloadstatuscallback-interface"></a>Interface IDODownloadStatusCallback

L’interface **IDODownloadStatusCallback** est utilisée pour recevoir des notifications relatives à un téléchargement.

## <a name="methods"></a>Méthodes

L’interface **IDODownloadStatusCallback** possède ces méthodes.

| Méthode | Description |
| ---- |:---- |
| [IDODownloadStatusCallback::OnStatusChanged](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | L’optimisation de la distribution appelle votre implémentation de cette méthode chaque fois qu’un état de téléchargement a changé. |

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |