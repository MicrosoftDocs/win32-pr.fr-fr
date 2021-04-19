---
description: Les certificats peuvent être demandés et distribués via n’importe quel mécanisme de transport.
ms.assetid: 2cbd0cdb-eefa-4434-893d-20e8b34f4cfe
title: Indépendance du transport
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8d68b8f6312495c242f6b2bd2ea75301f802c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521434"
---
# <a name="transport-independence"></a><span data-ttu-id="1e3b4-103">Indépendance du transport</span><span class="sxs-lookup"><span data-stu-id="1e3b4-103">Transport Independence</span></span>

<span data-ttu-id="1e3b4-104">Les certificats peuvent être demandés et distribués via n’importe quel mécanisme de transport.</span><span class="sxs-lookup"><span data-stu-id="1e3b4-104">Certificates can be requested and distributed through any transport mechanism.</span></span> <span data-ttu-id="1e3b4-105">Les services de certificats acceptent les [*demandes de certificat*](../secgloss/c-gly.md) d’un demandeur via http, DCOM, RPC, un fichier disque ou un transport personnalisé.</span><span class="sxs-lookup"><span data-stu-id="1e3b4-105">Certificate Services accepts [*certificate requests*](../secgloss/c-gly.md) from an applicant through HTTP, DCOM, RPC, disk file, or by custom transport.</span></span> <span data-ttu-id="1e3b4-106">Les services de certificats publient des certificats au demandeur via HTTP, DCOM, RPC, un fichier de disque ou un transport personnalisé.</span><span class="sxs-lookup"><span data-stu-id="1e3b4-106">Certificate Services posts certificates to the applicant through HTTP, DCOM, RPC, disk file, or custom transport.</span></span>

<span data-ttu-id="1e3b4-107">Les transports sont pris en charge par les applications intermédiaires et les dll du module de sortie, généralement écrites en C/C++.</span><span class="sxs-lookup"><span data-stu-id="1e3b4-107">Transports are supported by intermediary applications and exit module DLLs, usually written in C/C++.</span></span> <span data-ttu-id="1e3b4-108">Les applications intermédiaires et les modules de sortie isolent les fonctions des services de certificats de la communication avec un transport spécifique.</span><span class="sxs-lookup"><span data-stu-id="1e3b4-108">The intermediary applications and exit modules isolate Certificate Services functions from communicating with any specific transport.</span></span>

 

 
