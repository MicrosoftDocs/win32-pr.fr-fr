---
title: Format du pilote installable
description: Format du pilote installable
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- pilotes installables, formats
- pilotes installables, fonction DriverProc
- pilotes installables, messages
- messages du pilote
- formats de pilote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fbbdcb8a49184dee6e9cf13c9f434506b1b48f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369031"
---
# <a name="installable-driver-format"></a>Format du pilote installable

Chaque pilote installable exporte une fonction [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) . Cette fonction de point d’entrée courante reçoit des *messages de pilote* du système qui indiquent au pilote d’effectuer des actions ou de fournir des informations. Le système envoie des messages de pilote à la fonction **DriverProc** lorsqu’une application ou une dll ouvre ou ferme le pilote ou demande qu’un message soit envoyé au pilote. La fonction **DriverProc** traite le message ou le transmet au gestionnaire de messages par défaut, à savoir la fonction [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) . Dans les deux cas, **DriverProc** doit retourner une valeur indiquant si l’action demandée a réussi.

 

 