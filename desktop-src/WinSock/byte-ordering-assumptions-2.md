---
description: Structures sockaddr et hypothèses de classement des octets dans Winsock.
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: Hypothèses de classement des octets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21c1e680b0fe658994723b0a1d87c2a7d6adbf0a00a5452b185401b03099089
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097909"
---
# <a name="byte-ordering-assumptions"></a>Hypothèses de classement des octets

Un fournisseur de services doit traiter tous les composants [**sockaddr**](sockaddr-2.md) en exclusivité du paramètre de famille d’adresses comme s’ils se trouvent dans l’ordre d’octet du réseau, et le paramètre de famille d’adresses comme dans l’ordre d’octet de l’ordinateur local. Il incombe à l’application Winsock de s’assurer que les adresses contenues dans les structures **sockaddr** sont correctement organisées. L’API Winsock fournit un certain nombre de routines de conversion pour simplifier cette tâche. Actuellement, ces routines comprennent la conversion entre l’ordre de l’octet naturel de l’hôte local et l’ordre des octets du réseau Big endian ou Little-endian. L’architecture Winsock peut prendre en charge d’autres schémas de classement des octets à l’avenir.

 

 



