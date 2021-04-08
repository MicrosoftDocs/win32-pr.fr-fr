---
description: La classe de l’appareil comm. est constituée de ports de communication. Vous accédez à ces appareils à l’aide des fonctions de fichier et de communication.
ms.assetid: c1cf4998-b752-4cfd-9dd7-c9872b62c44b
title: comm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40136654d7e308f30e4e27467cf5e21385340841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752997"
---
# <a name="comm"></a><span data-ttu-id="fde70-104">comm</span><span class="sxs-lookup"><span data-stu-id="fde70-104">comm</span></span>

<span data-ttu-id="fde70-105">La classe de l’appareil comm. est constituée de ports de communication.</span><span class="sxs-lookup"><span data-stu-id="fde70-105">The comm device class consists of communications ports.</span></span> <span data-ttu-id="fde70-106">Vous accédez à ces appareils à l’aide des [fonctions](/windows/desktop/DevIO/communications-functions)de [fichier](/windows/desktop/FileIO/file-management-functions) et de communication.</span><span class="sxs-lookup"><span data-stu-id="fde70-106">You access these devices by using the [file](/windows/desktop/FileIO/file-management-functions) and [communications functions](/windows/desktop/DevIO/communications-functions).</span></span>

<span data-ttu-id="fde70-107">La fonction [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) remplit une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **DWSTRINGFORMAT** sur la \_ valeur ASCII STRINGFORMAT et en ajoutant une chaîne terminée par le caractère null qui spécifie le nom de l’appareil de communication (par exemple, le nom du modem).</span><span class="sxs-lookup"><span data-stu-id="fde70-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_ASCII value and appending a null-terminated string that specifies the name of the communication device (such as the modem name).</span></span>

 

 
