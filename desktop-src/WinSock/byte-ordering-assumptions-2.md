---
description: Structures sockaddr et hypothèses de classement des octets dans Winsock.
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: Hypothèses de classement des octets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe6abf9ed46302bd037d1eb130b18c5568518cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514612"
---
# <a name="byte-ordering-assumptions"></a>Hypothèses de classement des octets

Un fournisseur de services doit traiter tous les composants [**sockaddr**](sockaddr-2.md) en exclusivité du paramètre de famille d’adresses comme s’ils se trouvent dans l’ordre d’octet du réseau, et le paramètre de famille d’adresses comme dans l’ordre d’octet de l’ordinateur local. Il incombe à l’application Winsock de s’assurer que les adresses contenues dans les structures **sockaddr** sont correctement organisées. L’API Winsock fournit un certain nombre de routines de conversion pour simplifier cette tâche. Actuellement, ces routines comprennent la conversion entre l’ordre de l’octet naturel de l’hôte local et l’ordre des octets du réseau Big endian ou Little-endian. L’architecture Winsock peut prendre en charge d’autres schémas de classement des octets à l’avenir.

 

 



