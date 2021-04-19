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
# <a name="byte-ordering-assumptions"></a><span data-ttu-id="23493-103">Hypothèses de classement des octets</span><span class="sxs-lookup"><span data-stu-id="23493-103">Byte Ordering Assumptions</span></span>

<span data-ttu-id="23493-104">Un fournisseur de services doit traiter tous les composants [**sockaddr**](sockaddr-2.md) en exclusivité du paramètre de famille d’adresses comme s’ils se trouvent dans l’ordre d’octet du réseau, et le paramètre de famille d’adresses comme dans l’ordre d’octet de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="23493-104">A service provider should treat all [**sockaddr**](sockaddr-2.md) components exclusive of the address family parameter as if they are in the network byte order, and the address family parameter as in the local computer's byte order.</span></span> <span data-ttu-id="23493-105">Il incombe à l’application Winsock de s’assurer que les adresses contenues dans les structures **sockaddr** sont correctement organisées.</span><span class="sxs-lookup"><span data-stu-id="23493-105">It is the Winsock application's responsibility to make sure that addresses contained in **sockaddr** structures are properly arranged.</span></span> <span data-ttu-id="23493-106">L’API Winsock fournit un certain nombre de routines de conversion pour simplifier cette tâche.</span><span class="sxs-lookup"><span data-stu-id="23493-106">The Winsock API provides a number of conversion routines to simplify this task.</span></span> <span data-ttu-id="23493-107">Actuellement, ces routines comprennent la conversion entre l’ordre de l’octet naturel de l’hôte local et l’ordre des octets du réseau Big endian ou Little-endian.</span><span class="sxs-lookup"><span data-stu-id="23493-107">Currently these routines understand conversion between the local host's natural byte order and either big-Endian or little-Endian network byte ordering.</span></span> <span data-ttu-id="23493-108">L’architecture Winsock peut prendre en charge d’autres schémas de classement des octets à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="23493-108">The Winsock architecture can support other byte ordering schemes in the future.</span></span>

 

 



