---
title: commande Open (Corecrt \_ IO. h)
description: La commande Open Initialise un appareil. Tous les périphériques MCI reconnaissent cette commande.
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- ouvrir la commande multimédia Windows
topic_type:
- apiref
api_name:
- open
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8d31f1806a9c12f764c679548564aa053c3041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741429"
---
# <a name="open-command"></a><span data-ttu-id="89c1a-105">ouvrir une commande</span><span class="sxs-lookup"><span data-stu-id="89c1a-105">open command</span></span>

<span data-ttu-id="89c1a-106">La commande Open Initialise un appareil.</span><span class="sxs-lookup"><span data-stu-id="89c1a-106">The open command initializes a device.</span></span> <span data-ttu-id="89c1a-107">Tous les périphériques MCI reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="89c1a-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="89c1a-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="89c1a-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("open %s %s %s"), 
  lpszDevice, 
  lpszOpenFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="89c1a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89c1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89c1a-110"><span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*</span><span class="sxs-lookup"><span data-stu-id="89c1a-110"><span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*</span></span>
</dt> <dd>

<span data-ttu-id="89c1a-111">Identificateur d’un périphérique MCI ou d’un pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="89c1a-111">Identifier of an MCI device or device driver.</span></span> <span data-ttu-id="89c1a-112">Il peut s’agir d’un nom d’appareil (comme indiqué dans le registre ou le fichier SYSTEM.INI) ou du nom de fichier du pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="89c1a-112">This can be either a device name (as given in the registry or the SYSTEM.INI file) or the filename of the device driver.</span></span> <span data-ttu-id="89c1a-113">Si vous spécifiez le nom de fichier du pilote de périphérique, vous pouvez éventuellement inclure le. DRV, mais vous ne devez pas inclure le chemin d’accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="89c1a-113">If you specify the filename of the device driver, you can optionally include the .DRV extension, but you should not include the path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="89c1a-114"><span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*</span><span class="sxs-lookup"><span data-stu-id="89c1a-114"><span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*</span></span>
</dt> <dd>

<span data-ttu-id="89c1a-115">Indicateur qui identifie l’élément à initialiser.</span><span class="sxs-lookup"><span data-stu-id="89c1a-115">Flag that identifies what to initialize.</span></span> <span data-ttu-id="89c1a-116">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Open** et les indicateurs utilisés par chaque type.</span><span class="sxs-lookup"><span data-stu-id="89c1a-116">The following table lists device types that recognize the **open** command and the flags used by each type.</span></span>



| <span data-ttu-id="89c1a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="89c1a-117">Value</span></span>        | <span data-ttu-id="89c1a-118">Signification</span><span class="sxs-lookup"><span data-stu-id="89c1a-118">Meaning</span></span>                                                        | <span data-ttu-id="89c1a-119">Signification</span><span class="sxs-lookup"><span data-stu-id="89c1a-119">Meaning</span></span>                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="89c1a-120">cdaudio</span><span class="sxs-lookup"><span data-stu-id="89c1a-120">cdaudio</span></span>      | <span data-ttu-id="89c1a-121">alias d' *appareil \_ alias* partageable</span><span class="sxs-lookup"><span data-stu-id="89c1a-121">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="89c1a-122">type *de \_ périphérique* de type</span><span class="sxs-lookup"><span data-stu-id="89c1a-122">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="89c1a-123">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="89c1a-123">digitalvideo</span></span> | <span data-ttu-id="89c1a-124">alias de l' *appareil \_ aliaselementname* nostatic parent *HWND* partageable</span><span class="sxs-lookup"><span data-stu-id="89c1a-124">alias *device\_aliaselementname* nostatic parent *hwnd* sharable</span></span> | <span data-ttu-id="89c1a-125">style de style d’un style enfant chevauchement style de style Popup type *de type \_* *périphérique \_*</span><span class="sxs-lookup"><span data-stu-id="89c1a-125">style child style overlapped style popup style *style\_type* type *device\_type*</span></span> |
| <span data-ttu-id="89c1a-126">superposition</span><span class="sxs-lookup"><span data-stu-id="89c1a-126">overlay</span></span>      | <span data-ttu-id="89c1a-127">alias de l' *appareil \_* alias parent du style partageable *HWND*</span><span class="sxs-lookup"><span data-stu-id="89c1a-127">alias *device\_alias* parent *hwnd* sharable style child</span></span>         | <span data-ttu-id="89c1a-128">style de style Popup style avec chevauchement style type *de type \_* *périphérique \_*</span><span class="sxs-lookup"><span data-stu-id="89c1a-128">style overlapped style popup style *style\_type* type *device\_type*</span></span>             |
| <span data-ttu-id="89c1a-129">sequencer</span><span class="sxs-lookup"><span data-stu-id="89c1a-129">sequencer</span></span>    | <span data-ttu-id="89c1a-130">alias d' *appareil \_ alias* partageable</span><span class="sxs-lookup"><span data-stu-id="89c1a-130">alias *device\_alias* sharable</span></span>                                 | <span data-ttu-id="89c1a-131">type *de \_ périphérique* de type</span><span class="sxs-lookup"><span data-stu-id="89c1a-131">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="89c1a-132">vidéo</span><span class="sxs-lookup"><span data-stu-id="89c1a-132">vcr</span></span>          | <span data-ttu-id="89c1a-133">alias d' *appareil \_ alias* partageable</span><span class="sxs-lookup"><span data-stu-id="89c1a-133">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="89c1a-134">type *de \_ périphérique* de type</span><span class="sxs-lookup"><span data-stu-id="89c1a-134">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="89c1a-135">videodisk</span><span class="sxs-lookup"><span data-stu-id="89c1a-135">videodisk</span></span>    | <span data-ttu-id="89c1a-136">alias d' *appareil \_ alias* partageable</span><span class="sxs-lookup"><span data-stu-id="89c1a-136">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="89c1a-137">type *de \_ périphérique* de type</span><span class="sxs-lookup"><span data-stu-id="89c1a-137">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="89c1a-138">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="89c1a-138">waveaudio</span></span>    | <span data-ttu-id="89c1a-139">alias de la *\_ taille* de la mémoire tampon des *\_ alias d’appareil*</span><span class="sxs-lookup"><span data-stu-id="89c1a-139">alias *device\_alias* buffer *buffer\_size*</span></span>                     | <span data-ttu-id="89c1a-140">*\_ type de périphérique* partageable</span><span class="sxs-lookup"><span data-stu-id="89c1a-140">sharable type *device\_type*</span></span>                                                    |



 

<span data-ttu-id="89c1a-141">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszOpenFlags** et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="89c1a-141">The following table lists the flags that can be specified in the **lpszOpenFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="89c1a-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="89c1a-142">Value</span></span>                 | <span data-ttu-id="89c1a-143">Signification</span><span class="sxs-lookup"><span data-stu-id="89c1a-143">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c1a-144">alias de l' *appareil \_* alias</span><span class="sxs-lookup"><span data-stu-id="89c1a-144">alias *device\_alias*</span></span> | <span data-ttu-id="89c1a-145">Spécifie un autre nom pour l’appareil donné.</span><span class="sxs-lookup"><span data-stu-id="89c1a-145">Specifies an alternate name for the given device.</span></span> <span data-ttu-id="89c1a-146">S’il est spécifié, il doit être utilisé *comme \_ ID d’appareil* dans les commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="89c1a-146">If specified, it must be used as the *device\_id* in subsequent commands.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="89c1a-147">*ElementName*</span><span class="sxs-lookup"><span data-stu-id="89c1a-147">*elementname*</span></span>         | <span data-ttu-id="89c1a-148">Spécifie le nom de l’élément d’appareil (fichier) chargé lorsque l’appareil s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="89c1a-148">Specifies the name of the device element (file) loaded when the device opens.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="89c1a-149">*\_ taille* de la mémoire tampon de mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="89c1a-149">buffer *buffer\_size*</span></span> | <span data-ttu-id="89c1a-150">Définit la taille, en secondes, de la mémoire tampon utilisée par le périphérique Wave-audio.</span><span class="sxs-lookup"><span data-stu-id="89c1a-150">Sets the size, in seconds, of the buffer used by the waveform-audio device.</span></span> <span data-ttu-id="89c1a-151">La taille par défaut de la mémoire tampon est définie lorsque le périphérique Wave-audio est installé ou configuré.</span><span class="sxs-lookup"><span data-stu-id="89c1a-151">The default size of the buffer is set when the waveform-audio device is installed or configured.</span></span> <span data-ttu-id="89c1a-152">En règle générale, la taille de la mémoire tampon est définie à 4 secondes.</span><span class="sxs-lookup"><span data-stu-id="89c1a-152">Typically the buffer size is set to 4 seconds.</span></span> <span data-ttu-id="89c1a-153">Avec l’appareil MCIWAVE, la taille minimale est de 2 secondes et la taille maximale est de 9 secondes.</span><span class="sxs-lookup"><span data-stu-id="89c1a-153">With the MCIWAVE device, the minimum size is 2 seconds and the maximum size is 9 seconds.</span></span>                                                |
| <span data-ttu-id="89c1a-154">*HWND* parent</span><span class="sxs-lookup"><span data-stu-id="89c1a-154">parent *hwnd*</span></span>         | <span data-ttu-id="89c1a-155">Spécifie le handle de fenêtre de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="89c1a-155">Specifies the window handle of the parent window.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="89c1a-156">partageable</span><span class="sxs-lookup"><span data-stu-id="89c1a-156">sharable</span></span>              | <span data-ttu-id="89c1a-157">Initialise l’appareil ou le fichier comme partageable.</span><span class="sxs-lookup"><span data-stu-id="89c1a-157">Initializes the device or file as sharable.</span></span> <span data-ttu-id="89c1a-158">Les tentatives suivantes d’ouverture du périphérique ou du fichier échouent, sauf si vous spécifiez « partageable » dans les commandes d’origine et les commandes **ouvertes** suivantes.</span><span class="sxs-lookup"><span data-stu-id="89c1a-158">Subsequent attempts to open the device or file fail unless you specify "sharable" in both the original and subsequent **open** commands.</span></span> <span data-ttu-id="89c1a-159">MCI retourne une erreur d’appareil non valide si l’appareil est déjà ouvert et ne peut pas être partagé.</span><span class="sxs-lookup"><span data-stu-id="89c1a-159">MCI returns an invalid device error if the device is already open and not sharable.</span></span><br/> <span data-ttu-id="89c1a-160">Les appareils MCISEQ Sequencer et MCIWAVE ne prennent pas en charge les fichiers partagés.</span><span class="sxs-lookup"><span data-stu-id="89c1a-160">The MCISEQ sequencer and MCIWAVE devices do not support shared files.</span></span><br/> |
| <span data-ttu-id="89c1a-161">enfant de style</span><span class="sxs-lookup"><span data-stu-id="89c1a-161">style child</span></span>           | <span data-ttu-id="89c1a-162">Ouvre une fenêtre avec un style de fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="89c1a-162">Opens a window with a child window style.</span></span>                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="89c1a-163">chevauchement de style</span><span class="sxs-lookup"><span data-stu-id="89c1a-163">style overlapped</span></span>      | <span data-ttu-id="89c1a-164">Ouvre une fenêtre avec un style de fenêtre avec chevauchement.</span><span class="sxs-lookup"><span data-stu-id="89c1a-164">Opens a window with an overlapped window style.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="89c1a-165">menu contextuel style</span><span class="sxs-lookup"><span data-stu-id="89c1a-165">style popup</span></span>           | <span data-ttu-id="89c1a-166">Ouvre une fenêtre avec un style de fenêtre contextuelle.</span><span class="sxs-lookup"><span data-stu-id="89c1a-166">Opens a window with a pop-up window style.</span></span>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="89c1a-167">*\_ type de style* de style</span><span class="sxs-lookup"><span data-stu-id="89c1a-167">style *style\_type*</span></span>   | <span data-ttu-id="89c1a-168">Indique un style de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="89c1a-168">Indicates a window style.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="89c1a-169">type *de \_ périphérique* de type</span><span class="sxs-lookup"><span data-stu-id="89c1a-169">type *device\_type*</span></span>   | <span data-ttu-id="89c1a-170">Spécifie le type d’appareil d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="89c1a-170">Specifies the device type of a file.</span></span>                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="89c1a-171"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="89c1a-171"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="89c1a-172">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="89c1a-172">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="89c1a-173">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="89c1a-173">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89c1a-174">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="89c1a-174">Return Value</span></span>

<span data-ttu-id="89c1a-175">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="89c1a-175">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="89c1a-176">Notes</span><span class="sxs-lookup"><span data-stu-id="89c1a-176">Remarks</span></span>

<span data-ttu-id="89c1a-177">MCI réserve « cdaudio » pour le type de périphérique CD audio, « videodisc » pour le type d’appareil videodisc, « Sequencer » pour le type d’appareil MIDI Sequencer, « AVIVideo » pour le type de périphérique vidéo numérique et « WaveAudio » pour le type de périphérique Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="89c1a-177">MCI reserves "cdaudio" for the CD audio device type, "videodisc" for the videodisc device type, "sequencer" for the MIDI sequencer device type, "AVIVideo" for the digital-video device type, and "waveaudio" for the waveform-audio device type.</span></span>

<span data-ttu-id="89c1a-178">En guise d’alternative à l’indicateur « type », MCI peut sélectionner l’appareil en fonction de l’extension utilisée par le fichier, tel qu’il est enregistré dans le registre ou dans la \[ \] section d’extension MCI du fichier SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="89c1a-178">As an alternative to the "type" flag, MCI can select the device based on the extension used by the file, as recorded in the registry or the \[mci extension\] section of the SYSTEM.INI file.</span></span>

<span data-ttu-id="89c1a-179">MCI peut ouvrir des fichiers AVI à l’aide d’un pointeur d’interface de fichier ou d’un pointeur d’interface de flux.</span><span class="sxs-lookup"><span data-stu-id="89c1a-179">MCI can open AVI files by using a file-interface pointer or a stream-interface pointer.</span></span> <span data-ttu-id="89c1a-180">Pour ouvrir un fichier à l’aide de l’un des deux types de pointeur d’interface, spécifiez un arobase (@) suivi du pointeur d’interface à la place du nom du fichier ou du périphérique pour le paramètre *lpszDevice* .</span><span class="sxs-lookup"><span data-stu-id="89c1a-180">To open a file by using either type of interface pointer, specify an at sign (@) followed by the interface pointer in place of the file or device name for the *lpszDevice* parameter.</span></span> <span data-ttu-id="89c1a-181">Pour plus d’informations sur les interfaces de fichier et de flux, consultez « [fonctions et macros avifile](avifile-functions-and-macros.md)».</span><span class="sxs-lookup"><span data-stu-id="89c1a-181">For more information about the file and stream interfaces, see " [AVIFile Functions and Macros](avifile-functions-and-macros.md)."</span></span>

<span data-ttu-id="89c1a-182">La commande suivante ouvre l’appareil « mySound ».</span><span class="sxs-lookup"><span data-stu-id="89c1a-182">The following command opens the "mysound" device.</span></span>

``` syntax
open new type waveaudio alias mysound buffer 6
```

<span data-ttu-id="89c1a-183">Avec le nom de périphérique « nouveau », le pilote de forme d’onde prépare une nouvelle ressource de forme d’onde.</span><span class="sxs-lookup"><span data-stu-id="89c1a-183">With device name "new", the waveform driver prepares a new waveform resource.</span></span> <span data-ttu-id="89c1a-184">La commande attribue l’alias d’appareil « mySound » et spécifie une mémoire tampon de 6 secondes.</span><span class="sxs-lookup"><span data-stu-id="89c1a-184">The command assigns the device alias "mysound" and specifies a 6-second buffer.</span></span>

<span data-ttu-id="89c1a-185">Vous pouvez éliminer l’indicateur « type » si vous combinez le nom de l’appareil avec le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="89c1a-185">You can eliminate the "type" flag if you combine the device name with the filename.</span></span> <span data-ttu-id="89c1a-186">MCI reconnaît cette combinaison lorsque vous utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="89c1a-186">MCI recognizes this combination when you use the following syntax:</span></span>

<span data-ttu-id="89c1a-187">*\_ nom* de l’appareil !</span><span class="sxs-lookup"><span data-stu-id="89c1a-187">*device\_name* !</span></span> <span data-ttu-id="89c1a-188">*nom de l’élément \_*</span><span class="sxs-lookup"><span data-stu-id="89c1a-188">*element\_name*</span></span>

<span data-ttu-id="89c1a-189">Le point d’exclamation sépare le nom du périphérique du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="89c1a-189">The exclamation point separates the device name from the filename.</span></span> <span data-ttu-id="89c1a-190">Le point d’exclamation ne doit pas être délimité par des espaces blancs.</span><span class="sxs-lookup"><span data-stu-id="89c1a-190">The exclamation point should not be delimited by white spaces.</span></span>

<span data-ttu-id="89c1a-191">L’exemple suivant ouvre le droit. Fichier WAV utilisant l’appareil « WaveAudio ».</span><span class="sxs-lookup"><span data-stu-id="89c1a-191">The following example opens the RIGHT.WAV file using the "waveaudio" device.</span></span>

``` syntax
open waveaudio!right.wav
```

<span data-ttu-id="89c1a-192">Le pilote MCIWAVE requiert un périphérique audio Wave asynchrone.</span><span class="sxs-lookup"><span data-stu-id="89c1a-192">The MCIWAVE driver requires an asynchronous waveform-audio device.</span></span>

## <a name="requirements"></a><span data-ttu-id="89c1a-193">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89c1a-193">Requirements</span></span>



| <span data-ttu-id="89c1a-194">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89c1a-194">Requirement</span></span> | <span data-ttu-id="89c1a-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="89c1a-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c1a-196">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89c1a-196">Minimum supported client</span></span><br/> | <span data-ttu-id="89c1a-197">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89c1a-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="89c1a-198">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89c1a-198">Minimum supported server</span></span><br/> | <span data-ttu-id="89c1a-199">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89c1a-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="89c1a-200">En-tête</span><span class="sxs-lookup"><span data-stu-id="89c1a-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="89c1a-201"><dt>Corecrt \_ IO. h</dt></span><span class="sxs-lookup"><span data-stu-id="89c1a-201"><dt>Corecrt\_io.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89c1a-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89c1a-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89c1a-203">MCI</span><span class="sxs-lookup"><span data-stu-id="89c1a-203">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="89c1a-204">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="89c1a-204">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

