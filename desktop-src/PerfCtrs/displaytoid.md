---
description: La table DisplayToID lie la chaîne conviviale affichée par le moniteur système au GUID stocké dans les autres tables.
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: DisplayToID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b71ae8c4ebaafc80d98580a13a83e3cc7cff815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519117"
---
# <a name="displaytoid"></a><span data-ttu-id="d4fdd-103">DisplayToID</span><span class="sxs-lookup"><span data-stu-id="d4fdd-103">DisplayToID</span></span>

<span data-ttu-id="d4fdd-104">La table **DisplayToID** lie la chaîne conviviale affichée par le moniteur système au GUID stocké dans les autres tables.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-104">The **DisplayToID** table relates the user-friendly string displayed by the System Monitor to the GUID stored in the other tables.</span></span>

<span data-ttu-id="d4fdd-105">La table **DisplayToID** définit les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="d4fdd-105">The **DisplayToID** table defines the following fields:</span></span>

-   <span data-ttu-id="d4fdd-106">**GUID :** Identificateur unique généré pour un journal.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-106">**GUID:** Unique identifier generated for a log.</span></span> <span data-ttu-id="d4fdd-107">Ce champ est la clé primaire de cette table.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-107">This field is the primary key of this table.</span></span>
-   <span data-ttu-id="d4fdd-108">**RunId :** Réservé à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-108">**RunID:** Reserved for internal use.</span></span>
-   <span data-ttu-id="d4fdd-109">**DisplayString :** Nom du fichier journal tel qu’il s’affiche dans le moniteur système.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-109">**DisplayString:** Name of the log file as displayed in the System Monitor.</span></span>
-   <span data-ttu-id="d4fdd-110">**LogStartTime :** Heure de début du processus de journalisation au format aaaa-mm-jj hh : mm : SS : nnn.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-110">**LogStartTime:** Time the logging process started in yyyy-mm-dd hh:mm:ss:nnn format.</span></span>
-   <span data-ttu-id="d4fdd-111">**LogStopTime :** Heure d’arrêt du processus de journalisation au format aaaa-mm-jj hh : mm : SS : nnn.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-111">**LogStopTime:** Time the logging process stopped in yyyy-mm-dd hh:mm:ss:nnn format.</span></span> <span data-ttu-id="d4fdd-112">Il est possible de différencier plusieurs fichiers journaux ayant la même valeur **DisplayString** à l’aide de la valeur de ce champ et des champs **LogStartTime** .</span><span class="sxs-lookup"><span data-stu-id="d4fdd-112">Multiple log files with the same **DisplayString** value can be differentiated by using the value in this and the **LogStartTime** fields.</span></span> <span data-ttu-id="d4fdd-113">Les valeurs des champs **LogStartTime** et **LogStopTime** permettent également d’accéder rapidement à la durée totale de collecte.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-113">The values in the **LogStartTime** and **LogStopTime** fields also allows the total collection time to be accessed quickly.</span></span>
-   <span data-ttu-id="d4fdd-114">**NumberOfRecords :** Nombre d’échantillons stockés dans la table pour chaque collection de journaux.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-114">**NumberOfRecords:** Number of samples stored in the table for each log collection.</span></span>
-   <span data-ttu-id="d4fdd-115">**MinutesToUTC :** Valeur utilisée pour convertir les données de ligne stockées en heure UTC en heure locale.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-115">**MinutesToUTC:** Value used to convert the row data stored in UTC time to local time.</span></span>
-   <span data-ttu-id="d4fdd-116">**TimeZoneName :** Nom du fuseau horaire dans lequel les données ont été collectées.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-116">**TimeZoneName:** Name of the time zone where the data was collected.</span></span> <span data-ttu-id="d4fdd-117">Si vous collectez ou que vous avez reconnecté des données à partir d’un fichier collecté sur des systèmes dans votre propre fuseau horaire, ce champ indique l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-117">If you are collecting or have relogged data from a file collected on systems in your own time zone, this field will state the location.</span></span>

<span data-ttu-id="d4fdd-118">**Remarque**  Avant Windows Vista, les ensembles de collecteurs de données étaient stockés dans le registre à l’adresse</span><span class="sxs-lookup"><span data-stu-id="d4fdd-118">**Note**  Prior to Windows Vista, the data collector sets were stored in the registry at</span></span>

<span data-ttu-id="d4fdd-119">**HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ services \\ SysmonLog \\ journaux des requêtes**</span><span class="sxs-lookup"><span data-stu-id="d4fdd-119">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\SysmonLog\\Log Queries**</span></span>

<span data-ttu-id="d4fdd-120">.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-120">.</span></span> <span data-ttu-id="d4fdd-121">Les champs listés ci-dessus ne correspondent pas aux valeurs du Registre.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-121">The fields listed above do not correspond to the values in registry.</span></span> <span data-ttu-id="d4fdd-122">Pour Windows Vista, les ensembles de collecteurs de données ne sont pas stockés dans le registre.</span><span class="sxs-lookup"><span data-stu-id="d4fdd-122">For Windows Vista, the data collector sets are not stored in the registry.</span></span>

 

 



