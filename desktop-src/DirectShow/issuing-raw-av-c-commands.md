---
description: Émission de commandes AV/C brutes
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: Émission de commandes AV/C brutes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1cf1b25d45a0eb35ede7151941d0cd49d30db0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392512"
---
# <a name="issuing-raw-avc-commands"></a><span data-ttu-id="23a65-103">Émission de commandes AV/C brutes</span><span class="sxs-lookup"><span data-stu-id="23a65-103">Issuing Raw AV/C Commands</span></span>

<span data-ttu-id="23a65-104">Les interfaces [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)et [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) fonctionnent en traduisant les appels de méthode en commandes pour le pilote, puis en interprétant la réponse du pilote et en la renvoyant via un **HRESULT** ou un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="23a65-104">The [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport), and [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) interfaces work by translating the method calls into commands for the driver, then interpreting the driver's response and returning it through an **HRESULT** or an output parameter.</span></span> <span data-ttu-id="23a65-105">Toutefois, certaines fonctions de l’appareil peuvent ne pas être accessibles par le biais de ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="23a65-105">However, some device functions may not be accessible through these methods.</span></span> <span data-ttu-id="23a65-106">Par conséquent, MSDV prend en charge l’envoi de commandes AV/C brutes à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="23a65-106">Therefore, MSDV supports sending raw AV/C commands to the device.</span></span>

<span data-ttu-id="23a65-107">Vous devez garder à l’esprit les points suivants lors de l’utilisation de cette fonctionnalité :</span><span class="sxs-lookup"><span data-stu-id="23a65-107">You should keep the following points in mind when using this feature:</span></span>

-   <span data-ttu-id="23a65-108">La commande est passée directement à l’appareil, sans vérification des erreurs ni validation de paramètre.</span><span class="sxs-lookup"><span data-stu-id="23a65-108">The command is passed directly to the device, with no error checking or parameter validation.</span></span> <span data-ttu-id="23a65-109">Pour cette raison, vous devez émettre des commandes AV/C brutes uniquement lorsque les interfaces DirectShow n’implémentent pas les fonctionnalités dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="23a65-109">For this reason, you should issue raw AV/C commands only when the DirectShow interfaces do not implement the functionality you need.</span></span>
-   <span data-ttu-id="23a65-110">Toutes les commandes AV/C brutes sont synchrones.</span><span class="sxs-lookup"><span data-stu-id="23a65-110">All raw AV/C commands are synchronous.</span></span> <span data-ttu-id="23a65-111">Le thread émettant la commande se bloque jusqu’à ce que la commande retourne.</span><span class="sxs-lookup"><span data-stu-id="23a65-111">The thread issuing the command blocks until the command returns.</span></span>
-   <span data-ttu-id="23a65-112">Une seule commande peut être donnée à la fois.</span><span class="sxs-lookup"><span data-stu-id="23a65-112">Only one command can be given at a time.</span></span> <span data-ttu-id="23a65-113">Pendant le traitement de la commande, l’appareil rejette toutes les commandes supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="23a65-113">While the command is being processed, the device will reject any additional commands.</span></span>
-   <span data-ttu-id="23a65-114">Le pilote UVC ne prend pas en charge les commandes AV/C brutes.</span><span class="sxs-lookup"><span data-stu-id="23a65-114">The UVC driver does not support raw AV/C commands.</span></span>

<span data-ttu-id="23a65-115">Pour envoyer une commande AV/C, mettez en forme la commande sous la forme d’un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="23a65-115">To send an AV/C command, format the command as an array of bytes.</span></span> <span data-ttu-id="23a65-116">Appelez ensuite [**IAMExtTransport :: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters).</span><span class="sxs-lookup"><span data-stu-id="23a65-116">Then call [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters).</span></span> <span data-ttu-id="23a65-117">Transmettez l' \_ indicateur Ed RAW \_ ext \_ dev \_ cmd, la taille du tableau et le tableau.</span><span class="sxs-lookup"><span data-stu-id="23a65-117">Pass in the ED\_RAW\_EXT\_DEV\_CMD flag, the array size, and the array.</span></span> <span data-ttu-id="23a65-118">Vous devez effectuer un cast de l’adresse du tableau en type \**LPOLESTR \** _, car l’objectif initial de ce paramètre était de retourner une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="23a65-118">You must cast the array address to an \**LPOLESTR\** _ type, because the original purpose of this parameter was to return a string value.</span></span>


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR_) AvcCmd);
```



<span data-ttu-id="23a65-119">Le contenu du tableau est transmis directement à l’appareil. vous devez donc veiller à le mettre en forme correctement.</span><span class="sxs-lookup"><span data-stu-id="23a65-119">The contents of the array are passed directly to the device, so you must be careful to format it correctly.</span></span> <span data-ttu-id="23a65-120">Une commande peut cibler l’unité (caméscope) ou une sous-unité (bande ou caméra).</span><span class="sxs-lookup"><span data-stu-id="23a65-120">A command can target the unit (camcorder) or a subunit (tape or camera).</span></span> <span data-ttu-id="23a65-121">Les normes pertinentes sont disponibles sur le [site Web 1394 Trade Association](https://1394ta.org).</span><span class="sxs-lookup"><span data-stu-id="23a65-121">The relevant standards are available from the [1394 Trade Association Web site](https://1394ta.org).</span></span>

-   <span data-ttu-id="23a65-122">Spécification générale du jeu de commandes de l’interface numérique AV/C</span><span class="sxs-lookup"><span data-stu-id="23a65-122">AV/C Digital Interface Command Set General Specification</span></span>
-   <span data-ttu-id="23a65-123">Spécification de la sous-unité d’enregistreur/lecteur de bande AV/C</span><span class="sxs-lookup"><span data-stu-id="23a65-123">AV/C Tape Recorder/Player Subunit Specification</span></span>

<span data-ttu-id="23a65-124">La première décrit comment mettre en forme des commandes AV/C et répertorie les commandes d’unité.</span><span class="sxs-lookup"><span data-stu-id="23a65-124">The former describes how to format AV/C commands and lists the unit commands.</span></span> <span data-ttu-id="23a65-125">La dernière spécification répertorie les commandes de sous-unité.</span><span class="sxs-lookup"><span data-stu-id="23a65-125">The latter specification lists the subunit commands.</span></span>

<span data-ttu-id="23a65-126">La méthode **GetTransportBasicParameters** peut retourner l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="23a65-126">The **GetTransportBasicParameters** method may return one of the following error codes:</span></span>



| <span data-ttu-id="23a65-127">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="23a65-127">Error Code</span></span>              | <span data-ttu-id="23a65-128">Description</span><span class="sxs-lookup"><span data-stu-id="23a65-128">Description</span></span>                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="23a65-129">\_délai d’erreur</span><span class="sxs-lookup"><span data-stu-id="23a65-129">ERROR\_TIMEOUT</span></span>          | <span data-ttu-id="23a65-130">La commande a expiré.</span><span class="sxs-lookup"><span data-stu-id="23a65-130">The command timed out.</span></span>                                                           |
| <span data-ttu-id="23a65-131">ERREUR \_ req \_ non \_ ACCEP</span><span class="sxs-lookup"><span data-stu-id="23a65-131">ERROR\_REQ\_NOT\_ACCEP</span></span>  | <span data-ttu-id="23a65-132">L’appareil n’a pas accepté la commande.</span><span class="sxs-lookup"><span data-stu-id="23a65-132">The device did not accept the command.</span></span>                                           |
| <span data-ttu-id="23a65-133">ERREUR \_ non \_ prise en charge</span><span class="sxs-lookup"><span data-stu-id="23a65-133">ERROR\_NOT\_SUPPORTED</span></span>   | <span data-ttu-id="23a65-134">L’appareil ne prend pas en charge la commande.</span><span class="sxs-lookup"><span data-stu-id="23a65-134">The device does not support the command.</span></span>                                         |
| <span data-ttu-id="23a65-135">demande d’erreur \_ \_ abandonnée</span><span class="sxs-lookup"><span data-stu-id="23a65-135">ERROR\_REQUEST\_ABORTED</span></span> | <span data-ttu-id="23a65-136">La commande a été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="23a65-136">The command was aborted.</span></span> <span data-ttu-id="23a65-137">Possbly l’appareil a été supprimé ou une réinitialisation du bus s’est produite.</span><span class="sxs-lookup"><span data-stu-id="23a65-137">Possbly the device was removed or a bus reset occurred.</span></span> |



 

> [!Note]  
> <span data-ttu-id="23a65-138">Ces erreurs sont retournées sous la forme de codes d’erreur Win32, et non HRESULT. vous devez donc tester ces valeurs directement, plutôt que d’utiliser les macros ayant **réussi** et **échoué** .</span><span class="sxs-lookup"><span data-stu-id="23a65-138">These errors are returned as Win32 error codes, not HRESULTs, so you should test for these values directly, rather than using the **SUCCEEDED** and **FAILED** macros.</span></span>

 

<span data-ttu-id="23a65-139">Si la méthode retourne la valeur \_ OK, la réponse de l’appareil est copiée dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="23a65-139">If the method returns S\_OK, the response from the device is copied into the array.</span></span> <span data-ttu-id="23a65-140">La charge utile de la réponse peut être plus grande que la commande. vous devez donc allouer une mémoire tampon suffisamment grande pour la conserver.</span><span class="sxs-lookup"><span data-stu-id="23a65-140">The response payload might be larger than the command, so you must allocate a buffer large enough to hold it.</span></span> <span data-ttu-id="23a65-141">La taille maximale de la charge utile est de 512 octets.</span><span class="sxs-lookup"><span data-stu-id="23a65-141">The maximum payload size is 512 bytes.</span></span> <span data-ttu-id="23a65-142">Notez qu’une valeur de retour de S \_ OK ne signifie pas toujours que l’appareil a correctement exécuté la commande.</span><span class="sxs-lookup"><span data-stu-id="23a65-142">Note that a return value of S\_OK does not always mean the device successfully carried out the command.</span></span> <span data-ttu-id="23a65-143">L’application doit examiner la charge utile de réponse pour déterminer l’État.</span><span class="sxs-lookup"><span data-stu-id="23a65-143">The application must examine the response payload to determine the status.</span></span>

<span data-ttu-id="23a65-144">L’exemple suivant illustre la commande permettant de rechercher une recherche de numéro de piste absolue :</span><span class="sxs-lookup"><span data-stu-id="23a65-144">The following example shows the command to search for an absolute track number search:</span></span>


```C++
// Set up the ATN search command.
BYTE AvcCmd[] = 
{ 
    0x00,   // ctype = "control"
    0x20,   // subunit_type, subunit_id
    0x52,   // opcode (ATN)
    0x20,   // operand 0 = "search"
    0x00,   // operand 1 = ATN
    0x00,   // operand 2 = ATN
    0x00,   // operand 3 = ATN
    0xFF   //  operand 4 = D-VCR medium type.
};
// Specify a track number.
ULONG ulTrackNumber = track_number; // Specify the track number here.
// Shift over by 1 (LSB of operand 1 is a 1-bit blank flag)
ulTrackNumber = ulTrackNumber << 1; 
// Plug this number into operands 1 - 3.
AvcCmd[4] = (BYTE) (ulTrackNumber & 0x000000FF);
AvcCmd[5] = (BYTE)((ulTrackNumber & 0x0000FF00) >> 8);
AvcCmd[6] = (BYTE)((ulTrackNumber & 0x00FF0000) >> 16);
```



## <a name="related-topics"></a><span data-ttu-id="23a65-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23a65-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23a65-146">Contrôle d’un caméscope DV</span><span class="sxs-lookup"><span data-stu-id="23a65-146">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



