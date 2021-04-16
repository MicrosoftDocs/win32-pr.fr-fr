---
description: Les développeurs de bases de données d’installation doivent être conscients de deux limitations sur la gestion des flux par l’implémentation de stockage structuré OLE Win32.
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: Limitations OLE sur les flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ccf2a259b004605381792a4eb9da62d329be91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201790"
---
# <a name="ole-limitations-on-streams"></a><span data-ttu-id="5299e-103">Limitations OLE sur les flux</span><span class="sxs-lookup"><span data-stu-id="5299e-103">OLE Limitations on Streams</span></span>

<span data-ttu-id="5299e-104">Les développeurs de bases de données d’installation doivent être conscients de deux limitations sur la gestion des flux par l’implémentation de stockage structuré OLE Win32.</span><span class="sxs-lookup"><span data-stu-id="5299e-104">Developers of installation databases need to be aware of two limitations on the handling of streams by the Win32 OLE structured storage implementation.</span></span> <span data-ttu-id="5299e-105">Ces limitations peuvent affecter les fonctions du programme d’installation indirectement par le biais de transformations et d’autres données qui peuvent être stockées dans la base de données sous forme de flux.</span><span class="sxs-lookup"><span data-stu-id="5299e-105">These limitations can affect installer functions indirectly through transforms and other data that may be stored in the database as a stream.</span></span>

<span data-ttu-id="5299e-106">Deux limitations s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="5299e-106">There are two relevant limitations:</span></span>

-   <span data-ttu-id="5299e-107">Les données binaires sont stockées avec un nom d’index créé en concaténant le nom de la table et les valeurs des clés primaires de l’enregistrement à l’aide d’un délimiteur de point.</span><span class="sxs-lookup"><span data-stu-id="5299e-107">Binary data is stored with an index name created by concatenating the table name and the values of the record's primary keys using a period delimiter.</span></span> <span data-ttu-id="5299e-108">OLE limite les noms de flux à 32 caractères (31 + terminateur null).</span><span class="sxs-lookup"><span data-stu-id="5299e-108">OLE limits stream names to 32 characters (31 + null terminator).</span></span> <span data-ttu-id="5299e-109">Windows Installer utilise un algorithme de compression qui peut étendre la limite à 62 caractères en fonction du caractère.</span><span class="sxs-lookup"><span data-stu-id="5299e-109">Windows Installer uses a compression algorithm that can expand the limit to 62 characters depending upon the character.</span></span> <span data-ttu-id="5299e-110">Notez que les caractères codés sur deux octets comptent comme 2.</span><span class="sxs-lookup"><span data-stu-id="5299e-110">Note that double-byte characters count as 2.</span></span>
-   <span data-ttu-id="5299e-111">Même si plusieurs flux peuvent être ouverts en même temps, vous ne pouvez pas ouvrir un flux une deuxième fois jusqu’à la fermeture de la première référence.</span><span class="sxs-lookup"><span data-stu-id="5299e-111">Although you can have multiple streams open at one time, you cannot open a stream a second time until the first reference is closed.</span></span> <span data-ttu-id="5299e-112">Cela signifie que vous ne pouvez pas sélectionner le même flux de données binaires à ouvrir simultanément dans plusieurs enregistrements.</span><span class="sxs-lookup"><span data-stu-id="5299e-112">This means you cannot select the same binary data stream to be open in multiple records simultaneously.</span></span> <span data-ttu-id="5299e-113">Les tentatives de lecture des données binaires à partir du deuxième enregistrement échouent.</span><span class="sxs-lookup"><span data-stu-id="5299e-113">Attempts to read the binary data from the second record fail.</span></span> <span data-ttu-id="5299e-114">Vous ne pouvez pas non plus renommer les clés primaires d’un enregistrement lorsqu’un flux de données binaires de cet enregistrement est ouvert.</span><span class="sxs-lookup"><span data-stu-id="5299e-114">Also you cannot rename the primary keys of a record while a binary data stream in that record is open.</span></span>

 

 



