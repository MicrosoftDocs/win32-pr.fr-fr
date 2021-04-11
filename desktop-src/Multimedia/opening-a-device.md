---
title: Ouverture d’un appareil
description: Ouverture d’un appareil
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- Commande MCI_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd975b0dd5004fb4b1209003568b7fd5901cfc4e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031089"
---
# <a name="opening-a-device"></a><span data-ttu-id="4a2f2-104">Ouverture d’un appareil</span><span class="sxs-lookup"><span data-stu-id="4a2f2-104">Opening a Device</span></span>

<span data-ttu-id="4a2f2-105">Avant d’utiliser un appareil, vous devez l’initialiser à l’aide de la commande [**ouvrir**](open.md) ([**MCI \_ Open**](mci-open.md)).</span><span class="sxs-lookup"><span data-stu-id="4a2f2-105">Before using a device, you must initialize it by using the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span> <span data-ttu-id="4a2f2-106">Cette commande charge le pilote dans la mémoire (s’il n’est pas déjà chargé) et récupère l’identificateur d’appareil que vous allez utiliser pour identifier l’appareil dans les commandes MCI suivantes.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-106">This command loads the driver into memory (if it isn't already loaded) and retrieves the device identifier you will use to identify the device in subsequent MCI commands.</span></span> <span data-ttu-id="4a2f2-107">Vous devez vérifier la valeur de retour de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) ou [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avant d’utiliser un nouvel identificateur d’appareil pour vous assurer que l’identificateur est valide.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-107">You should check the return value of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) or [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function before using a new device identifier to ensure that the identifier is valid.</span></span> <span data-ttu-id="4a2f2-108">(Vous pouvez également récupérer un identificateur d’appareil à l’aide de la fonction [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) .)</span><span class="sxs-lookup"><span data-stu-id="4a2f2-108">(You can also retrieve a device identifier by using the [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) function.)</span></span>

<span data-ttu-id="4a2f2-109">Comme tous les messages de commande MCI, l' **\_ ouverture de MCI** a une structure associée.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-109">Like all MCI command messages, **MCI\_OPEN** has an associated structure.</span></span> <span data-ttu-id="4a2f2-110">Ces structures sont parfois appelées des *blocs de paramètres*.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-110">These structures are sometimes called *parameter blocks*.</span></span> <span data-ttu-id="4a2f2-111">La structure par défaut pour **MCI \_ ouverte** est [**MCI \_ Open \_ PARMS**](mci-open-parms.md).</span><span class="sxs-lookup"><span data-stu-id="4a2f2-111">The default structure for **MCI\_OPEN** is [**MCI\_OPEN\_PARMS**](mci-open-parms.md).</span></span> <span data-ttu-id="4a2f2-112">Certains appareils (tels que *la forme d’onde* et la *superposition*) ont des structures étendues (telles que les paramètres [**\_ \_ Open Wave \_ MCI**](mci-wave-open-parms.md) et les paramètres d' [**\_ \_ ouverture OVLY Open \_ parms**](mci-ovly-open-parms.md)) pour prendre en charge des paramètres facultatifs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-112">Certain devices (such as *waveform* and *overlay*) have extended structures (such as [**MCI\_WAVE\_OPEN\_PARMS**](mci-wave-open-parms.md) and [**MCI\_OVLY\_OPEN\_PARMS**](mci-ovly-open-parms.md)) to accommodate additional optional parameters.</span></span> <span data-ttu-id="4a2f2-113">À moins que vous n’ayez besoin d’utiliser ces paramètres supplémentaires, vous pouvez utiliser la structure **\_ Open \_ PARMS des MCI** avec n’importe quel périphérique MCI.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-113">Unless you need to use these additional parameters, you can use the **MCI\_OPEN\_PARMS** structure with any MCI device.</span></span>

<span data-ttu-id="4a2f2-114">Le nombre d’appareils que vous pouvez ouvrir est limité uniquement par la quantité de mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-114">The number of devices you can have open is limited only by the amount of available memory.</span></span>

## <a name="using-an-alias"></a><span data-ttu-id="4a2f2-115">Utilisation d’un alias</span><span class="sxs-lookup"><span data-stu-id="4a2f2-115">Using an Alias</span></span>

<span data-ttu-id="4a2f2-116">Lorsque vous ouvrez un appareil, vous pouvez utiliser l’indicateur « alias » pour spécifier un identificateur de périphérique pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-116">When you open a device, you can use the "alias" flag to specify a device identifier for the device.</span></span> <span data-ttu-id="4a2f2-117">Cet indicateur vous permet d’attribuer un identificateur d’appareil abrégé pour les appareils composés avec des noms de fichiers longs, et il vous permet d’ouvrir plusieurs instances du même fichier ou périphérique.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-117">This flag lets you assign a short device identifier for compound devices with lengthy filenames, and it lets you open multiple instances of the same file or device.</span></span>

<span data-ttu-id="4a2f2-118">Par exemple, la commande suivante attribue l’identificateur d’appareil « birdcall » au nom de fichier de base C : \\ NABIRDS \\ Sounds \\ MOCKMTNG. WAV</span><span class="sxs-lookup"><span data-stu-id="4a2f2-118">For example, the following command assigns the device identifier "birdcall" to the lengthy filename C:\\NABIRDS\\SOUNDS\\MOCKMTNG.WAV:</span></span>


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="4a2f2-119">Dans l’interface de message de commande, vous spécifiez un alias à l’aide du membre **lpstrAlias** de la structure des [**\_ \_ PARMS Open PARMS**](mci-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="4a2f2-119">In the command-message interface, you specify an alias by using the **lpstrAlias** member of the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span>

## <a name="specifying-a-device-type"></a><span data-ttu-id="4a2f2-120">Spécification d’un type d’appareil</span><span class="sxs-lookup"><span data-stu-id="4a2f2-120">Specifying a Device Type</span></span>

<span data-ttu-id="4a2f2-121">Lorsque vous ouvrez un appareil, vous pouvez utiliser l’indicateur « type » pour faire référence à un type d’appareil, plutôt qu’à un pilote de périphérique spécifique.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-121">When you open a device, you can use the "type" flag to refer to a device type, rather than to a specific device driver.</span></span> <span data-ttu-id="4a2f2-122">L’exemple suivant ouvre le fichier Waveform-Audio C : \\ Windows \\ carillon. WAV (à l’aide de l’indicateur « type » pour spécifier le type d’appareil **WaveAudio** ) et attribue l’alias « carillons » :</span><span class="sxs-lookup"><span data-stu-id="4a2f2-122">The following example opens the waveform-audio file C:\\WINDOWS\\CHIMES.WAV (using the "type" flag to specify the **waveaudio** device type) and assigns the alias "chimes":</span></span>


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="4a2f2-123">Dans l’interface de message de commande, les fonctionnalités de l’indicateur « type » sont fournies par le membre **lpstrDeviceType** de la structure des fonctions [**\_ Open \_ PARMS de MCI**](mci-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="4a2f2-123">In the command-message interface, the functionality of the "type" flag is supplied by the **lpstrDeviceType** member of the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span>

## <a name="simple-and-compound-devices"></a><span data-ttu-id="4a2f2-124">Appareils simples et composés</span><span class="sxs-lookup"><span data-stu-id="4a2f2-124">Simple and Compound Devices</span></span>

<span data-ttu-id="4a2f2-125">MCI classifie les pilotes de périphériques comme *composés* ou *simples*.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-125">MCI classifies device drivers as *compound* or *simple*.</span></span> <span data-ttu-id="4a2f2-126">Les pilotes pour les appareils composés nécessitent le nom d’un fichier de données pour la lecture. les pilotes pour les périphériques simples ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-126">Drivers for compound devices require the name of a data file for playback; drivers for simple devices do not.</span></span>

<span data-ttu-id="4a2f2-127">Les appareils simples incluent des appareils **cdaudio** et **videodisc** .</span><span class="sxs-lookup"><span data-stu-id="4a2f2-127">Simple devices include **cdaudio** and **videodisc** devices.</span></span> <span data-ttu-id="4a2f2-128">Il existe deux façons d’ouvrir des appareils simples :</span><span class="sxs-lookup"><span data-stu-id="4a2f2-128">There are two ways to open simple devices:</span></span>

-   <span data-ttu-id="4a2f2-129">Spécifiez un pointeur vers une chaîne se terminant par un caractère null qui contient le nom de l’appareil à partir du registre ou du fichier SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-129">Specify a pointer to a null-terminated string containing the device name from the registry or the SYSTEM.INI file.</span></span>

    <span data-ttu-id="4a2f2-130">Par exemple, vous pouvez ouvrir un appareil **videodisc** à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4a2f2-130">For example, you can open a **videodisc** device by using the following command:</span></span>


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="4a2f2-131">Dans ce cas, « videodisc » est le nom de l’appareil à partir du registre ou \[ \] de la section mci de SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-131">In this case, "videodisc" is the device name from the registry or the \[mci\] section of SYSTEM.INI.</span></span>

-   <span data-ttu-id="4a2f2-132">Spécifiez le nom réel du pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-132">Specify the actual name of the device driver.</span></span> <span data-ttu-id="4a2f2-133">Toutefois, l’ouverture d’un appareil à l’aide du nom de fichier du pilote de périphérique rend l’application spécifique au périphérique et peut empêcher l’application de s’exécuter en cas de modification de la configuration du système.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-133">Opening a device using the device-driver filename, however, makes the application device-specific and can prevent the application from running if the system configuration changes.</span></span> <span data-ttu-id="4a2f2-134">Si vous utilisez un nom de fichier, vous n’avez pas besoin de spécifier le chemin d’accès complet ou l’extension de nom de fichier ; MCI suppose que les pilotes se trouvent dans un répertoire système et ont le. Nom de l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-134">If you use a filename, you do not need to specify the complete path or the filename extension; MCI assumes drivers are located in a system directory and have the .DRV filename extension.</span></span>

<span data-ttu-id="4a2f2-135">Les appareils composés comprennent les **WaveAudio** et les appareils **Sequencer** .</span><span class="sxs-lookup"><span data-stu-id="4a2f2-135">Compound devices include **waveaudio** and **sequencer** devices.</span></span> <span data-ttu-id="4a2f2-136">Les données d’un appareil composé sont parfois appelées *éléments d’appareil*.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-136">The data for a compound device is sometimes called a *device element*.</span></span> <span data-ttu-id="4a2f2-137">Toutefois, ce document fait généralement référence à ces données sous la forme d’un fichier, même si, dans certains cas, les données peuvent ne pas être stockées sous forme de fichier.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-137">This document, however, generally refers to this data as a file, even though in some cases the data might not be stored as a file.</span></span>

<span data-ttu-id="4a2f2-138">Il existe trois façons d’ouvrir un appareil composé :</span><span class="sxs-lookup"><span data-stu-id="4a2f2-138">There are three ways to open a compound device:</span></span>

-   <span data-ttu-id="4a2f2-139">Spécifiez uniquement le nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-139">Specify only the device name.</span></span> <span data-ttu-id="4a2f2-140">Cela vous permet d’ouvrir un appareil composé sans associer de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-140">This lets you open a compound device without associating a filename.</span></span> <span data-ttu-id="4a2f2-141">La plupart des appareils composés traitent uniquement les commandes de [**capacité**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) et de [**fermeture**](close.md) ([**MCI \_ Close**](mci-close.md)) lorsqu’ils sont ouverts de cette manière.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-141">Most compound devices process only the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)) and [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)) commands when they are opened this way.</span></span>
-   <span data-ttu-id="4a2f2-142">Spécifiez uniquement le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-142">Specify only the filename.</span></span> <span data-ttu-id="4a2f2-143">Le nom de l’appareil est déterminé à partir des associations du Registre.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-143">The device name is determined from the associations in the registry.</span></span>
-   <span data-ttu-id="4a2f2-144">Spécifiez le nom du fichier et le nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-144">Specify the filename and the device name.</span></span> <span data-ttu-id="4a2f2-145">MCI ignore les entrées dans le registre et ouvre le nom de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-145">MCI ignores the entries in the registry and opens the specified device name.</span></span>

<span data-ttu-id="4a2f2-146">Pour associer un fichier de données à un appareil particulier, vous pouvez spécifier le nom de fichier et le nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-146">To associate a data file with a particular device, you can specify the filename and device name.</span></span> <span data-ttu-id="4a2f2-147">Par exemple, la commande suivante ouvre l’appareil **WaveAudio** avec le nom de fichier MYVOICE. SND</span><span class="sxs-lookup"><span data-stu-id="4a2f2-147">For example, the following command opens the **waveaudio** device with the filename MYVOICE.SND:</span></span>


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="4a2f2-148">Dans l’interface de chaîne de commande, vous pouvez également abréger la spécification de nom de périphérique à l’aide du format de point d’exclamation alternatif, comme indiqué dans la commande [**ouvrir**](open.md) .</span><span class="sxs-lookup"><span data-stu-id="4a2f2-148">In the command-string interface, you can also abbreviate the device name specification by using the alternative exclamation-point format, as documented with the [**open**](open.md) command.</span></span>

## <a name="opening-a-device-using-the-filename-extension"></a><span data-ttu-id="4a2f2-149">Ouverture d’un appareil à l’aide de l’extension de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="4a2f2-149">Opening a Device Using the Filename Extension</span></span>

<span data-ttu-id="4a2f2-150">Si la commande [**ouvrir**](open.md) ([**MCI \_ Open**](mci-open.md)) spécifie uniquement le nom de fichier, MCI utilise l’extension de nom de fichier pour sélectionner l’appareil approprié dans la liste du registre ou dans la \[ \] section des extensions MCI du fichier SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-150">If the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command specifies only the filename, MCI uses the filename extension to select the appropriate device from the list in the registry or the \[mci extensions\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="4a2f2-151">Les entrées de la \[ section des extensions MCI \] utilisent la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="4a2f2-151">The entries in the \[mci extensions\] section use the following form:</span></span>

<span data-ttu-id="4a2f2-152">nom du périphérique d' *\_ extension de nom de fichier*  =  *\_*</span><span class="sxs-lookup"><span data-stu-id="4a2f2-152">*filename\_extension* = *device\_name*</span></span>

<span data-ttu-id="4a2f2-153">MCI utilise implicitement *le \_ nom* de l’appareil si l’extension est trouvée et si un nom de périphérique n’a pas été spécifié dans la commande **ouvrir** .</span><span class="sxs-lookup"><span data-stu-id="4a2f2-153">MCI implicitly uses *device\_name* if the extension is found and if a device name has not been specified in the **open** command.</span></span>

<span data-ttu-id="4a2f2-154">L’exemple suivant montre une \[ section d’extensions MCI standard \] :</span><span class="sxs-lookup"><span data-stu-id="4a2f2-154">The following example shows a typical \[mci extensions\] section:</span></span>


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



<span data-ttu-id="4a2f2-155">À l’aide de ces définitions, MCI ouvre l’appareil **WaveAudio** si la commande suivante est émise :</span><span class="sxs-lookup"><span data-stu-id="4a2f2-155">Using these definitions, MCI opens the **waveaudio** device if the following command is issued:</span></span>


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a><span data-ttu-id="4a2f2-156">Nouveaux fichiers de données</span><span class="sxs-lookup"><span data-stu-id="4a2f2-156">New Data Files</span></span>

<span data-ttu-id="4a2f2-157">Pour créer un nouveau fichier de données, spécifiez simplement un nom de fichier vide.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-157">To create a new data file, simply specify a blank filename.</span></span> <span data-ttu-id="4a2f2-158">MCI n’enregistre pas un nouveau fichier tant que vous ne l’avez pas enregistré à l’aide de la commande [**Enregistrer**](save.md) ([**\_ enregistrement MCI**](mci-save.md)).</span><span class="sxs-lookup"><span data-stu-id="4a2f2-158">MCI does not save a new file until you save it by using the [**save**](save.md) ([**MCI\_SAVE**](mci-save.md)) command.</span></span> <span data-ttu-id="4a2f2-159">Lorsque vous créez un fichier, vous devez inclure un alias d’appareil avec la commande [**ouvrir**](open.md) ([**MCI \_ Open**](mci-open.md)).</span><span class="sxs-lookup"><span data-stu-id="4a2f2-159">When creating a new file, you must include a device alias with the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span>

<span data-ttu-id="4a2f2-160">L’exemple suivant ouvre un nouveau fichier **WaveAudio** , démarre et arrête l’enregistrement, puis enregistre et ferme le fichier :</span><span class="sxs-lookup"><span data-stu-id="4a2f2-160">The following example opens a new **waveaudio** file, starts and stops recording, then saves and closes the file:</span></span>


```C++
mciSendString("open new type waveaudio alias capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("record capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("stop capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("save capture orca.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="sharable-devices"></a><span data-ttu-id="4a2f2-161">Appareils partageables</span><span class="sxs-lookup"><span data-stu-id="4a2f2-161">Sharable Devices</span></span>

<span data-ttu-id="4a2f2-162">L’indicateur « partageable » (MCI \_ Open \_ Shared) de la commande [**ouverte**](open.md) ([**MCI \_ Open**](mci-open.md)) permet à plusieurs applications d’accéder simultanément au même appareil (ou fichier) et à l’instance d’appareil.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-162">The "sharable" (MCI\_OPEN\_SHAREABLE) flag of the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command lets multiple applications access the same device (or file) and device instance simultaneously.</span></span> <span data-ttu-id="4a2f2-163">Si votre application ouvre un appareil ou un fichier comme partageable, d’autres applications peuvent également y accéder en l’ouvrant comme partageable.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-163">If your application opens a device or file as sharable, other applications can also access it by opening it as sharable.</span></span> <span data-ttu-id="4a2f2-164">L’appareil ou le fichier partagé donne à chaque application la possibilité de modifier les paramètres régissant son état d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-164">The shared device or file gives each application the ability to change the parameters governing its operating state.</span></span> <span data-ttu-id="4a2f2-165">Chaque fois qu’un appareil ou un fichier est ouvert en tant que partageable, MCI retourne un identificateur d’appareil unique, même si les identificateurs font référence à la même instance.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-165">Each time a device or file is opened as sharable, MCI returns a unique device identifier, even though the identifiers refer to the same instance.</span></span>

<span data-ttu-id="4a2f2-166">Si votre application ouvre un appareil ou un fichier sans spécifier qu’elle est partageable, aucune autre application ne peut y accéder jusqu’à ce que votre application la ferme.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-166">If your application opens a device or file without specifying that it is sharable, no other application can access it until your application closes it.</span></span> <span data-ttu-id="4a2f2-167">En outre, si un appareil ne prend en charge qu’une seule instance ouverte, la commande **Open** échoue si vous spécifiez l’indicateur partageable.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-167">Also, if a device supports only one open instance, the **open** command will fail if you specify the sharable flag.</span></span>

<span data-ttu-id="4a2f2-168">Si votre application ouvre un appareil et spécifie qu’il peut être partagé, votre application ne doit pas faire d’hypothèses concernant l’état de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-168">If your application opens a device and specifies that it is sharable, your application should not make any assumptions about the state of this device.</span></span> <span data-ttu-id="4a2f2-169">Votre application peut avoir besoin de compenser les modifications apportées par d’autres applications qui accèdent à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-169">Your application might need to compensate for changes made by other applications accessing the device.</span></span>

<span data-ttu-id="4a2f2-170">La plupart des fichiers composés ne peuvent pas être partagés ; Toutefois, vous pouvez ouvrir plusieurs fichiers, ou vous pouvez ouvrir un seul fichier à la fois.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-170">Most compound files are not sharable; however, you can open multiple files, or you can open a single file multiple times.</span></span> <span data-ttu-id="4a2f2-171">Si vous ouvrez un seul fichier à plusieurs moments, MCI crée une instance indépendante pour chaque instance, chaque instance ayant un état de fonctionnement unique.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-171">If you open a single file multiple times, MCI creates an independent instance for each, with each instance having a unique operating status.</span></span>

<span data-ttu-id="4a2f2-172">Si vous ouvrez plusieurs instances d’un fichier, vous devez assigner un identificateur d’appareil unique à chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-172">If you open multiple instances of a file, you must assign a unique device identifier to each.</span></span> <span data-ttu-id="4a2f2-173">Vous pouvez utiliser un alias, comme décrit dans la section suivante, pour attribuer un nom unique à chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="4a2f2-173">You can use an alias, as described in the following section, to assign a unique name for each file.</span></span>

 

 