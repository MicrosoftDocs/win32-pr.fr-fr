---
description: La fonction DuplicateHandle crée un handle dupliqué qui peut être utilisé par un autre processus spécifié.
ms.assetid: b79d2b8f-931e-4cab-9bbe-9ead1b102132
title: Duplication d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f8e0948ce55f5d25d7567346ecdec97f04b24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034846"
---
# <a name="object-duplication"></a><span data-ttu-id="1d454-103">Duplication d’objets</span><span class="sxs-lookup"><span data-stu-id="1d454-103">Object Duplication</span></span>

<span data-ttu-id="1d454-104">La fonction [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) crée un handle dupliqué qui peut être utilisé par un autre processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="1d454-104">The [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function creates a duplicate handle that can be used by another specified process.</span></span> <span data-ttu-id="1d454-105">Cette méthode de partage des handles d’objets est plus complexe que l’utilisation d’objets nommés ou de l’héritage.</span><span class="sxs-lookup"><span data-stu-id="1d454-105">This method of sharing object handles is more complex than using named objects or inheritance.</span></span> <span data-ttu-id="1d454-106">Elle nécessite une communication entre le processus de création et le processus dans lequel le descripteur est dupliqué.</span><span class="sxs-lookup"><span data-stu-id="1d454-106">It requires communication between the creating process and the process into which the handle is duplicated.</span></span> <span data-ttu-id="1d454-107">Les informations nécessaires (valeur de handle et identificateur de processus) peuvent être communiquées par les méthodes de communication interprocessus, telles que les canaux nommés ou la mémoire partagée nommée.</span><span class="sxs-lookup"><span data-stu-id="1d454-107">The necessary information (the handle value and process identifier) can be communicated by any of the interprocess communication methods, such as named pipes or named shared memory.</span></span>

 

 
