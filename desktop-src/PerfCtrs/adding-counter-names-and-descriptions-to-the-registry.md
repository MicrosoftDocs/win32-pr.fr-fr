---
description: Les noms et les descriptions de tous les objets de performance et de leurs compteurs sont stockés dans le registre.
ms.assetid: 6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4
title: Ajout de noms de compteurs et de descriptions au Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d2c97ebe80a8ef2a8396ca42583cbad874859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525061"
---
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a><span data-ttu-id="503bb-103">Ajout de noms de compteurs et de descriptions au Registre</span><span class="sxs-lookup"><span data-stu-id="503bb-103">Adding Counter Names and Descriptions to the Registry</span></span>

> [!IMPORTANT]
> <span data-ttu-id="503bb-104">En raison des limitations de performances et de fiabilité significatives, la méthode permettant de fournir des données de compteurs de performances que cette rubrique décrit peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="503bb-104">Due to significant performance and reliability limitations, the method for providing performance counter data that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="503bb-105">Au lieu de cela, Microsoft vous recommande d’utiliser la méthode décrite dans la rubrique [fourniture de données de compteur à l’aide de la Version 2,0](providing-counter-data-using-version-2-0.md) pour la création de nouveaux compteurs de performances et la migration des compteurs de performances existants pour utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="503bb-105">Instead, Microsoft recommends that you use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md) for creating new performance counters and that you migrate existing performance counters to use that method.</span></span>

<span data-ttu-id="503bb-106">Les noms et les descriptions de tous les objets de performance v1 et de leurs compteurs doivent être installés sur le système.</span><span class="sxs-lookup"><span data-stu-id="503bb-106">The names and descriptions of all V1 performance objects and their counters must be installed the system.</span></span> <span data-ttu-id="503bb-107">Pour stocker les noms et les descriptions des objets et des compteurs de votre [fournisseur v1](providing-counter-data.md):</span><span class="sxs-lookup"><span data-stu-id="503bb-107">To store names and descriptions for the objects and counters from your [V1 provider](providing-counter-data.md):</span></span>

- <span data-ttu-id="503bb-108">[Créez un fichier d’en-tête. h](#creating-a-symbolic-constants-h-file) contenant les constantes symboliques pour les décalages de vos objets et compteurs.</span><span class="sxs-lookup"><span data-stu-id="503bb-108">[Create a .h header file](#creating-a-symbolic-constants-h-file) that contains the symbolic constants for the offsets to your objects and counters.</span></span>
- <span data-ttu-id="503bb-109">[Créez une initialisation (. INI)](#creating-an-initialization-ini-file) qui contient les chaînes.</span><span class="sxs-lookup"><span data-stu-id="503bb-109">[Create an initialization (.INI) file](#creating-an-initialization-ini-file) that contains the strings.</span></span>
- <span data-ttu-id="503bb-110">Lors de l’installation de votre composant, [Exécutez l’outil **lodctr**](#running-the-lodctr-tool) pour installer les noms et les descriptions dans le registre.</span><span class="sxs-lookup"><span data-stu-id="503bb-110">When installing your component, [run the **lodctr** tool](#running-the-lodctr-tool) to install the names and descriptions into the registry.</span></span>
- <span data-ttu-id="503bb-111">Lors de la désinstallation de votre composant, exécutez l’outil unlodctr pour supprimer les noms et les descriptions du Registre.</span><span class="sxs-lookup"><span data-stu-id="503bb-111">When uninstalling your component, run the unlodctr tool to remove the names and descriptions from the registry.</span></span>

## <a name="creating-a-symbolic-constants-h-file"></a><span data-ttu-id="503bb-112">Création d’un fichier de constantes symboliques (. h)</span><span class="sxs-lookup"><span data-stu-id="503bb-112">Creating a symbolic constants (.h) file</span></span>

<span data-ttu-id="503bb-113">Créez un fichier d’en-tête. h qui définit les constantes (macros) des décalages aux objets et aux compteurs fournis par votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="503bb-113">Create a .h header file that defines constants (macros) for the offsets to the objects and counters that your provider provides.</span></span> <span data-ttu-id="503bb-114">L’en-tête. h est utilisé comme entrée pour **lodctr** pendant l’installation de votre fournisseur et peut également être utilisé par le code C/C++ de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="503bb-114">The .h header is used as input to **lodctr** during installation of your provider, and may also be used by the C/C++ code of your provider.</span></span>

<span data-ttu-id="503bb-115">Les valeurs de constante doivent être consécutives, même les nombres commençant par zéro.</span><span class="sxs-lookup"><span data-stu-id="503bb-115">The constant values must be consecutive, even numbers beginning with zero.</span></span> <span data-ttu-id="503bb-116">Regroupez les constantes par objets (par exemple, démarrez chaque groupe avec le décalage de l’objet, puis suivez les décalages des compteurs pour cet objet).</span><span class="sxs-lookup"><span data-stu-id="503bb-116">Group the constants by objects (i.e. start each group with the object offset, then follow with the offsets of the counters for that object).</span></span>

<span data-ttu-id="503bb-117">Les constantes dans l’en-tête déterminent l’ordre dans lequel les compteurs sont ajoutés au nom et au texte d’aide dans le registre.</span><span class="sxs-lookup"><span data-stu-id="503bb-117">The constants in the header determine the order in which the counters are added to the name and help text in the registry.</span></span> <span data-ttu-id="503bb-118">Le fournisseur utilise les offsets pour déterminer l’objet interrogé et les valeurs d’index à utiliser lors du retour des données.</span><span class="sxs-lookup"><span data-stu-id="503bb-118">The provider uses the offsets to determine which object is being queried and the index values to use when returning the data.</span></span> <span data-ttu-id="503bb-119">Pour plus d’informations, consultez [implémentation de OpenPerformanceData](implementing-openperformancedata.md).</span><span class="sxs-lookup"><span data-stu-id="503bb-119">For details, see [Implementing OpenPerformanceData](implementing-openperformancedata.md).</span></span>

<span data-ttu-id="503bb-120">L’exemple suivant illustre un fichier de constante symbolique, nommé CounterOffsets. h, qui est utilisé dans l’exemple [création d’une DLL d’extension de performances](creating-a-performance-extension-dll.md) .</span><span class="sxs-lookup"><span data-stu-id="503bb-120">The following shows an example of a symbolic constant file, named CounterOffsets.h, that is used in the [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md) example.</span></span>

```C++
#ifndef OFFSETS_H
#define OFFSETS_H

// Symbol file that defines constant values for the objects
// and counters that the provider provides. The counters should be
// grouped by object.

#define TRANSFER_OBJECT      0 // First object must be at offset 0.
#define BYTES_SENT           2 // Counters for the object follow.
#define AVAILABLE_BANDWIDTH  4 // Offsets must be even numbers.

// Not required, but for convenience in implementing the Open function:
#define LAST_TRANSFER_OBJECT_COUNTER_OFFSET  AVAILABLE_BANDWIDTH

#define PEER_OBJECT          6 // Second object must be at the next offset.
#define BYTES_SERVED         8 // Counter for the second object.

// Not required, but for convenience in implementing the Open function:
#define LAST_PEER_OBJECT_COUNTER_OFFSET  BYTES_SERVED

#endif // OFFSETS_H
```

## <a name="creating-an-initialization-ini-file"></a><span data-ttu-id="503bb-121">Création d’une initialisation (. Fichier INI)</span><span class="sxs-lookup"><span data-stu-id="503bb-121">Creating an initialization (.INI) file</span></span>

<span data-ttu-id="503bb-122">L’initialisation (. INI) contient le nom et les chaînes d’aide pour chaque objet et compteur définis dans votre fichier de symboles.</span><span class="sxs-lookup"><span data-stu-id="503bb-122">The initialization (.INI) file contains the name and help strings for each object and counter defined in your symbol file.</span></span> <span data-ttu-id="503bb-123">La. Le fichier INI est utilisé comme entrée pour **lodctr** lors de l’installation de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="503bb-123">The .INI file is used as input to **lodctr** during installation of your provider.</span></span>

<span data-ttu-id="503bb-124">La. Le fichier INI doit être encodé au format UTF-16LE (avec la marque d’ordre d’octet) et doit contenir les sections et les clés suivantes :</span><span class="sxs-lookup"><span data-stu-id="503bb-124">The .INI file should be encoded as UTF-16LE (with byte order mark) and should have the following sections and keys:</span></span>

```ini
[info]
drivername=ServiceKeyName
symbolfile=SymbolFile.h
trusted=(Unused)

[objects]
<symbol>_<langid>_NAME=(Unused)

[languages]
<langid>=(Unused)

[text]
<symbol>_<langid>_NAME=Name
<symbol>_<langid>_HELP=Description
```

### <a name="info-section"></a><span data-ttu-id="503bb-125">section [info]</span><span class="sxs-lookup"><span data-stu-id="503bb-125">[info] section</span></span>

<span data-ttu-id="503bb-126">La `[info]` section contient des informations générales sur le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="503bb-126">The `[info]` section contains general information about the provider.</span></span> <span data-ttu-id="503bb-127">Les clés de section sont définies comme suit :</span><span class="sxs-lookup"><span data-stu-id="503bb-127">The section keys are defined as follows:</span></span>

|<span data-ttu-id="503bb-128">Clé</span><span class="sxs-lookup"><span data-stu-id="503bb-128">Key</span></span>|<span data-ttu-id="503bb-129">Description</span><span class="sxs-lookup"><span data-stu-id="503bb-129">Description</span></span>
|---|-----------
|<span data-ttu-id="503bb-130">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="503bb-130">**DriverName**</span></span>| <span data-ttu-id="503bb-131">Spécifiez le nom de la clé de performance du fournisseur située dans le Registre sous la `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` clé.</span><span class="sxs-lookup"><span data-stu-id="503bb-131">Specify the name of the provider's performance key located in the registry under the `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` key.</span></span> <span data-ttu-id="503bb-132">Pour plus d’informations sur la création de cette clé, consultez [création de la clé de performance de l’application](creating-the-applications-performance-key.md).</span><span class="sxs-lookup"><span data-stu-id="503bb-132">For information on creating this key, see [Creating the Application's Performance Key](creating-the-applications-performance-key.md).</span></span>
|<span data-ttu-id="503bb-133">**SymbolFile**</span><span class="sxs-lookup"><span data-stu-id="503bb-133">**SymbolFile**</span></span>| <span data-ttu-id="503bb-134">Spécifiez le fichier d’en-tête. h qui contient les valeurs symboliques des objets et des compteurs de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="503bb-134">Specify the .h header file that contains symbolic values of your provider's objects and counters.</span></span> <span data-ttu-id="503bb-135">Pendant l’installation (lors de l’appel de **lodctr**), le fichier d’en-tête doit se trouver dans le même répertoire que le. Fichier INI.</span><span class="sxs-lookup"><span data-stu-id="503bb-135">During installation (when invoking **lodctr**), the header file must be in the same directory as the .INI file.</span></span>
|<span data-ttu-id="503bb-136">**TPM**</span><span class="sxs-lookup"><span data-stu-id="503bb-136">**Trusted**</span></span>| <span data-ttu-id="503bb-137">Si vous incluez cette clé dans la `[info]` section, **lodctr** ajoute une valeur de registre de code de validation de bibliothèque à votre clé de performance avec une signature binaire de votre dll de performance.</span><span class="sxs-lookup"><span data-stu-id="503bb-137">If you include this key in the `[info]` section, **lodctr** will add a Library Validation Code registry value to your performance key with a binary signature of your performance DLL.</span></span> <span data-ttu-id="503bb-138">Lorsque PERFLIB appelle votre DLL, il compare la signature avec votre DLL pour déterminer si la DLL a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="503bb-138">When PERFLIB calls your DLL it compares the signature with your DLL to determine if the DLL has been modified.</span></span> <span data-ttu-id="503bb-139">La valeur de la clé **approuvée** est ignorée.</span><span class="sxs-lookup"><span data-stu-id="503bb-139">The value of the **Trusted** key is ignored.</span></span>

<span data-ttu-id="503bb-140">Les `DriverName` `SymbolFile` clés et sont requises.</span><span class="sxs-lookup"><span data-stu-id="503bb-140">The `DriverName` and `SymbolFile` keys are required.</span></span>

### <a name="objects-section"></a><span data-ttu-id="503bb-141">section [objets]</span><span class="sxs-lookup"><span data-stu-id="503bb-141">[objects] section</span></span>

<span data-ttu-id="503bb-142">La `[objects]` section fournit une liste des objets de performance que le fournisseur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="503bb-142">The `[objects]` section provides a list of the performance objects that the provider supports.</span></span> <span data-ttu-id="503bb-143">Utilisé pour déterminer si chaque symbole de la `[text]` section fait référence à un objet ou à un compteur.</span><span class="sxs-lookup"><span data-stu-id="503bb-143">This is used to determine whether each symbol from the `[text]` section refers an object or a counter.</span></span>

<span data-ttu-id="503bb-144">Pour chaque objet (CounterSet) pris en charge par votre fournisseur, ajoutez une clé nommée `<symbol>_<langid>_NAME=` à la `[objects]` section, où `<symbol>` est le nom de l’objet et `<langid>` est l’ID de langue de l’une des langues prises en charge.</span><span class="sxs-lookup"><span data-stu-id="503bb-144">For each object (counterset) supported by your provider, add one key named `<symbol>_<langid>_NAME=` to the `[objects]` section, where `<symbol>` is the name of the object and `<langid>` is the language id of one of the supported languages.</span></span> <span data-ttu-id="503bb-145">La valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="503bb-145">The value is ignored.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="503bb-146">La `[objects]` section améliore les performances du système.</span><span class="sxs-lookup"><span data-stu-id="503bb-146">The `[objects]` section improves the performance of the system.</span></span> <span data-ttu-id="503bb-147">Bien que la section objets soit facultative, vous devez toujours inclure cette section dans votre. Fichier INI.</span><span class="sxs-lookup"><span data-stu-id="503bb-147">Although the objects section is optional, you should always include this section in your .INI file.</span></span> <span data-ttu-id="503bb-148">Si vous incluez cette section, votre DLL de performance est appelée uniquement si vous prenez en charge l’objet demandé.</span><span class="sxs-lookup"><span data-stu-id="503bb-148">If you include this section, your performance DLL is called only if you support the requested object.</span></span> <span data-ttu-id="503bb-149">Si vous n’incluez pas la section objets, votre DLL est appelée pour chaque requête, car le système ne connaît pas les objets pris en charge par votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="503bb-149">If you do not include the objects section, your DLL is called for every query because the system does not know which objects your provider supports.</span></span> <span data-ttu-id="503bb-150">Si la section de l’objet n’est pas incluse, **lodctr** génère un message dans le journal des événements de l’application, indiquant que le. Le fichier INI ne contient pas de section objets.</span><span class="sxs-lookup"><span data-stu-id="503bb-150">If the object section is not included, **lodctr** generates a message in the application event log stating that the .INI file did not contain an objects section.</span></span> <span data-ttu-id="503bb-151">L’identificateur d’événement de ce message est 2000.</span><span class="sxs-lookup"><span data-stu-id="503bb-151">The event identifier of this message is 2000.</span></span>

### <a name="languages-section"></a><span data-ttu-id="503bb-152">section [languages]</span><span class="sxs-lookup"><span data-stu-id="503bb-152">[languages] section</span></span>

<span data-ttu-id="503bb-153">La `[languages]` section fournit une liste des identificateurs de langue de chaque langue pour laquelle votre fournisseur fournit des chaînes de nom et d’aide.</span><span class="sxs-lookup"><span data-stu-id="503bb-153">The `[languages]` section provides a list of the language identifiers of each language for which your provider supplies name and help strings.</span></span> <span data-ttu-id="503bb-154">Tous les fournisseurs doivent prendre en charge `009` (anglais).</span><span class="sxs-lookup"><span data-stu-id="503bb-154">All providers should support `009` (English).</span></span>

<span data-ttu-id="503bb-155">Pour chaque langue prise en charge, ajoutez une clé nommée `<langid>=` .</span><span class="sxs-lookup"><span data-stu-id="503bb-155">For each supported language, add one key named `<langid>=`.</span></span> <span data-ttu-id="503bb-156">La valeur est ignorée, mais à des fins de documentation, la valeur est normalement définie sur le nom de la langue correspondante, par exemple `009=English` .</span><span class="sxs-lookup"><span data-stu-id="503bb-156">The value is ignored, but for documentation purposes the value is normally set to the name of the corresponding language, e.g. `009=English`.</span></span>

<span data-ttu-id="503bb-157">Pour la plupart des langues, vous devez utiliser l’identificateur de langue principal.</span><span class="sxs-lookup"><span data-stu-id="503bb-157">For most languages, you should use the primary language identifier.</span></span> <span data-ttu-id="503bb-158">La liste complète des identificateurs de langue se trouve dans le fichier d’en-tête Winnt. h, sous le titre « ID de langue principale ».</span><span class="sxs-lookup"><span data-stu-id="503bb-158">The complete list of language identifiers is in the Winnt.h header file, under the heading "Primary Language Ids."</span></span> <span data-ttu-id="503bb-159">Convertit la valeur trouvée dans Winnt. h en une séquence de 3 chiffres hexadécimaux en supprimant le `0x` préfixe et en ajoutant des chiffres de début `0` jusqu’à ce que la séquence ait une longueur de 3 chiffres.</span><span class="sxs-lookup"><span data-stu-id="503bb-159">Convert the value found in Winnt.h into a sequence of 3 hexadecimal digits by removing the `0x` prefix and adding leading `0` digits until the sequence is 3 digits long.</span></span> <span data-ttu-id="503bb-160">Par exemple, pour spécifier des chaînes en anglais (0x9), utilisez 009.</span><span class="sxs-lookup"><span data-stu-id="503bb-160">For example, to specify English strings (0x9), use 009.</span></span> <span data-ttu-id="503bb-161">Pour spécifier des chaînes italiennes (0x10), utilisez 010.</span><span class="sxs-lookup"><span data-stu-id="503bb-161">To specify Italian strings (0x10), use 010.</span></span>

<span data-ttu-id="503bb-162">Les langages chinois et portugais nécessitent à la fois les identificateurs principal et de sous-langue.</span><span class="sxs-lookup"><span data-stu-id="503bb-162">Chinese and Portuguese languages require both the primary and sublanguage identifiers.</span></span> <span data-ttu-id="503bb-163">Utilisez 404, 804, 416 ou 816 au lieu de 004 ou 016.</span><span class="sxs-lookup"><span data-stu-id="503bb-163">Use 404, 804, 416, or 816 instead of 004 or 016.</span></span>

### <a name="text-section"></a><span data-ttu-id="503bb-164">section [Text]</span><span class="sxs-lookup"><span data-stu-id="503bb-164">[text] section</span></span>

<span data-ttu-id="503bb-165">La `[text]` section fournit le nom et les chaînes d’aide pour vos objets et compteurs.</span><span class="sxs-lookup"><span data-stu-id="503bb-165">The `[text]` section provides the name and help strings for your objects and counters.</span></span>

<span data-ttu-id="503bb-166">Pour chaque objet ou compteur, et pour chaque langue prise en charge, vous devez fournir une clé de nom (contenant le nom ou la chaîne de titre pour votre objet ou compteur) et vous pouvez éventuellement fournir une clé d’aide (contenant la description ou la chaîne d’explication pour votre objet ou compteur).</span><span class="sxs-lookup"><span data-stu-id="503bb-166">For each object or counter, and for each supported language, you must provide a NAME key (containing the name or title string for your object or counter) and you may optionally provide a HELP key (containing the description or explanation string for your object or counter).</span></span> <span data-ttu-id="503bb-167">Les clés doivent être nommées `<symbol>_<langid>_NAME` et `<symbol>_<langid>_HELP` , où `<symbol>` est la constante symbolique pour l’objet ou le compteur (tel que défini dans le fichier. h de constante symbolique) et `<langid>` est l’identificateur de langue utilisé pour cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="503bb-167">The keys should be named `<symbol>_<langid>_NAME` and `<symbol>_<langid>_HELP`, where `<symbol>` is the symbolic constant for the object or counter (as defined in the symbolic constant .h file), and `<langid>` is the language identifier used for this string.</span></span>

<span data-ttu-id="503bb-168">Par exemple, les chaînes en anglais pour un compteur avec Symbol `MY_COUNTER` sont spécifiées comme suit :</span><span class="sxs-lookup"><span data-stu-id="503bb-168">For example, the English strings for a counter with symbol `MY_COUNTER` would be specified as:</span></span>

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

<span data-ttu-id="503bb-169">Les touches de texte peuvent apparaître dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="503bb-169">The text keys can appear in any order.</span></span> <span data-ttu-id="503bb-170">Les chaînes de texte ne doivent pas contenir de caractères de mise en forme tels que des tabulations.</span><span class="sxs-lookup"><span data-stu-id="503bb-170">The text strings should not contain formatting characters such as tabs.</span></span>

### <a name="example-ini-file"></a><span data-ttu-id="503bb-171">Exemple de fichier INI</span><span class="sxs-lookup"><span data-stu-id="503bb-171">Example INI file</span></span>

<span data-ttu-id="503bb-172">Voici un exemple de fichier d’initialisation utilisé dans l’exemple de [création d’une DLL d’extension de performances](creating-a-performance-extension-dll.md) .</span><span class="sxs-lookup"><span data-stu-id="503bb-172">The following is an example of an initialization file that is used in the [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md) sample.</span></span>

```ini
[info]
drivername=MyApplication
symbolfile=CounterOffsets.h
trusted=

[objects]
TRANSFER_OBJECT_009_NAME=
PEER_OBJECT_009_NAME=

[languages]
009=English
00C=French

[text]

// English strings

TRANSFER_OBJECT_009_NAME=Transfer
TRANSFER_OBJECT_009_HELP=Provides information related to transferring files.

BYTES_SENT_009_NAME=Bytes Sent
BYTES_SENT_009_HELP=Number of bytes sent in the last transfer.

AVAILABLE_BANDWIDTH_009_NAME=Available Bandwidth
AVAILABLE_BANDWIDTH_009_HELP=Available bandwidth on the network, in bytes.

PEER_OBJECT_009_NAME=Peer
PEER_OBJECT_009_HELP=Provides information related to peer-caching.

BYTES_SERVED_009_NAME=Bytes Served
BYTES_SERVED_009_HELP=Number of bytes served from the cache.

// French strings

TRANSFER_OBJECT_00C_NAME=Transfert
TRANSFER_OBJECT_00C_HELP=Fournit des informations liées aux transferts de fichiers.

BYTES_SENT_00C_NAME=Octets Envoyés
BYTES_SENT_00C_HELP=Nombre d'octets envoyés dans le dernier transfert.

AVAILABLE_BANDWIDTH_00C_NAME=Bande Passante Disponible
AVAILABLE_BANDWIDTH_00C_HELP=Bande passante disponible sur le réseau, en octets.

PEER_OBJECT_00C_NAME=Pair
PEER_OBJECT_00C_HELP=Fournit des informations liées é mise en cache homologue.

BYTES_SERVED_00C_NAME=Octets Servis
BYTES_SERVED_00C_HELP=Le nombre d'octets servis du cache.
```

## <a name="running-the-lodctr-tool"></a><span data-ttu-id="503bb-173">Exécution de l’outil lodctr</span><span class="sxs-lookup"><span data-stu-id="503bb-173">Running the Lodctr tool</span></span>

<span data-ttu-id="503bb-174">Pour charger les noms et les chaînes d’aide définis dans votre. Fichier INI (au cours de l’installation de votre fournisseur), exécutez l’outil **lodctr** à partir du dossier qui contient votre. Fichier INI et fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="503bb-174">To load the names and help strings defined in your .INI file (during the installation of your provider), run the **lodctr** tool from the folder that contains your .INI file and header file.</span></span> <span data-ttu-id="503bb-175">L’outil est inclus avec l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="503bb-175">The tool is included with the computer.</span></span> <span data-ttu-id="503bb-176">Vous devez exécuter **lodctr** avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="503bb-176">You must run **lodctr** with elevated privileges.</span></span> <span data-ttu-id="503bb-177">Le paramètre de **lodctr** est le chemin d’accès à votre. Fichier INI.</span><span class="sxs-lookup"><span data-stu-id="503bb-177">The parameter to **lodctr** is the path to your .INI file.</span></span> <span data-ttu-id="503bb-178">Par exemple : `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.</span><span class="sxs-lookup"><span data-stu-id="503bb-178">For example, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.</span></span>

<span data-ttu-id="503bb-179">Pour décharger les chaînes de noms et d’aide (pendant la désinstallation), exécutez l’outil **unlodctr** .</span><span class="sxs-lookup"><span data-stu-id="503bb-179">To unload the names and help strings (during uninstall), run the **unlodctr** tool.</span></span> <span data-ttu-id="503bb-180">Vous devez exécuter **unlodctr** avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="503bb-180">You must run **unlodctr** with elevated privileges.</span></span> <span data-ttu-id="503bb-181">Le paramètre de **unlodctr** est le DriverName de votre fournisseur (nom de la clé de performance du fournisseur).</span><span class="sxs-lookup"><span data-stu-id="503bb-181">The parameter to **unlodctr** is the DriverName of your provider (the name of the provider's performance key).</span></span> <span data-ttu-id="503bb-182">Par exemple : `unlodctr "MyProvider"`.</span><span class="sxs-lookup"><span data-stu-id="503bb-182">For example, `unlodctr "MyProvider"`.</span></span>

<span data-ttu-id="503bb-183">Avant d’exécuter **lodctr**, assurez-vous que votre application comporte une entrée sous la clé **services** .</span><span class="sxs-lookup"><span data-stu-id="503bb-183">Before running **lodctr**, be sure that your application has an entry under the **Services** key.</span></span> <span data-ttu-id="503bb-184">Pour plus d’informations, consultez [création de la clé de performance de l’application](creating-the-applications-performance-key.md).</span><span class="sxs-lookup"><span data-stu-id="503bb-184">For details, see [Creating the Application's Performance Key](creating-the-applications-performance-key.md).</span></span> <span data-ttu-id="503bb-185">Si la clé n’existe pas, **lodctr** ne met pas à jour le Registre avec vos noms et descriptions.</span><span class="sxs-lookup"><span data-stu-id="503bb-185">If the key does not exist, **lodctr** will not update the registry with your names and descriptions.</span></span>

<span data-ttu-id="503bb-186">Comme alternative à l’exécution de **lodctr**, vous pouvez appeler [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (défini dans loadperf. h) à partir de votre programme d’installation pour charger les descriptions des noms de compteur.</span><span class="sxs-lookup"><span data-stu-id="503bb-186">As an alternative to running **lodctr**, you can call [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (defined in Loadperf.h) from your installation program to load your counter names descriptions.</span></span> <span data-ttu-id="503bb-187">Vous pouvez ensuite appeler [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) pendant la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="503bb-187">You can then call [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) during uninstall.</span></span>

<span data-ttu-id="503bb-188">L’utilitaire **lodctr** copie les chaînes à partir du. INI vers les **compteurs** et les valeurs de registre de l' **aide** sous les sous-clés de langue appropriées.</span><span class="sxs-lookup"><span data-stu-id="503bb-188">The **lodctr** utility copies the strings from the .INI file to the **Counters** and **Help** registry values under the appropriate language subkeys.</span></span> <span data-ttu-id="503bb-189">Si la sous-clé de langue correspondante n’existe pas, les chaînes de cette langue ne sont pas copiées.</span><span class="sxs-lookup"><span data-stu-id="503bb-189">If the corresponding language subkey does not exist, the strings for that language are not copied.</span></span> <span data-ttu-id="503bb-190">L’utilitaire met également à jour le **dernier compteur** et la **dernière valeur d’aide** .</span><span class="sxs-lookup"><span data-stu-id="503bb-190">The utility also updates the **Last Counter** and **Last Help** value.</span></span> <span data-ttu-id="503bb-191">Les noms et les descriptions des compteurs de performances sont stockés à l’emplacement suivant dans le registre.</span><span class="sxs-lookup"><span data-stu-id="503bb-191">The performance counter names and descriptions are stored in the following location in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = highest counter index
                  Last Help = highest help index
                  \009
                     Counters = 2 System 4 Memory...
                     Help = 3 The System Object Type...
                  \supported language, other than English
                     Counters = ...
                     Help = ...
```

<span data-ttu-id="503bb-192">Outre l’ajout de valeurs sous la clé **Perflib** , l’outil **lodctr** ajoute également les valeurs suivantes au nœud **services** de l’application.</span><span class="sxs-lookup"><span data-stu-id="503bb-192">In addition to adding values under the **PerfLib** key, the **lodctr** tool also adds the following values to the **Services** node for the application.</span></span> <span data-ttu-id="503bb-193">Dans la plupart des cas, l’application et le fournisseur auront une relation un-à-un. Toutefois, un fournisseur peut fournir des données de compteur pour plusieurs applications, ce qui explique pourquoi la clé est basée sur l’application et non sur le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="503bb-193">In most cases, the application and provider will have a one-to-one relationship; however, it is possible for a provider to provide counter data for multiple applications, which is why the key is based on the application and not the provider.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \MyApplication
               \Performance
                  First Counter = lowest counter index assigned to provider
                  First Help = lowest help index assigned to provider
                  Last Counter = highest counter index assigned to provider
                  Last Help = highest help index assigned to provider
                  Object List = list of object index values if the .INI includes the [objects] section
                  Library Validation Code = if the [info] section contains a "trusted" key
```
