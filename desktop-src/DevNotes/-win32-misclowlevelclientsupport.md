---
description: Cette rubrique contient des informations sur les API de bas niveau utilisées par l’infrastructure cliente Windows.
ms.assetid: 14a6e970-2032-420e-9930-a15909dbbb97
title: Prise en charge des clients de Low-Level divers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11558c9994a9c622f71e803521352d1073e68c05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846917"
---
# <a name="miscellaneous-low-level-client-support"></a><span data-ttu-id="de7b0-103">Prise en charge des clients de Low-Level divers</span><span class="sxs-lookup"><span data-stu-id="de7b0-103">Miscellaneous Low-Level Client Support</span></span>

<span data-ttu-id="de7b0-104">Cette rubrique contient des informations sur les API de bas niveau utilisées par l’infrastructure cliente Windows.</span><span class="sxs-lookup"><span data-stu-id="de7b0-104">This topic contains information about low-level APIs that are used by the Windows client infrastructure.</span></span>

### <a name="functions"></a><span data-ttu-id="de7b0-105">Fonctions</span><span class="sxs-lookup"><span data-stu-id="de7b0-105">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de7b0-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="de7b0-106">Topic</span></span></th>
<th><span data-ttu-id="de7b0-107">Contenu</span><span class="sxs-lookup"><span data-stu-id="de7b0-107">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de7b0-108"><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-108"><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-109">La fonction _lclose ferme le fichier spécifié afin qu’il ne soit plus disponible pour la lecture ou l’écriture.</span><span class="sxs-lookup"><span data-stu-id="de7b0-109">The _lclose function closes the specified file so that it is no longer available for reading or writing.</span></span> <span data-ttu-id="de7b0-110">Cette fonction est fournie à des fins de compatibilité avec les versions 16 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="de7b0-110">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="de7b0-111">Les applications Win32 doivent utiliser la fonction CloseHandle.</span><span class="sxs-lookup"><span data-stu-id="de7b0-111">Win32-based applications should use the CloseHandle function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7b0-112"><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-112"><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-113">La fonction _lopen ouvre un fichier existant et définit le pointeur de fichier au début du fichier.</span><span class="sxs-lookup"><span data-stu-id="de7b0-113">The _lopen function opens an existing file and sets the file pointer to the beginning of the file.</span></span> <span data-ttu-id="de7b0-114">Cette fonction est fournie à des fins de compatibilité avec les versions 16 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="de7b0-114">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="de7b0-115">Les applications Win32 doivent utiliser la fonction CreateFile.</span><span class="sxs-lookup"><span data-stu-id="de7b0-115">Win32-based applications should use the CreateFile function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de7b0-116"><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-116"><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-117">La fonction _lread lit les données du fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="de7b0-117">The _lread function reads data from the specified file.</span></span> <span data-ttu-id="de7b0-118">Cette fonction est fournie à des fins de compatibilité avec les versions 16 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="de7b0-118">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="de7b0-119">Les applications Win32 doivent utiliser la fonction ReadFile.</span><span class="sxs-lookup"><span data-stu-id="de7b0-119">Win32-based applications should use the ReadFile function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7b0-120"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-120"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-121">Retourne une valeur indiquant si les codecs DVD sont activés sur l’appareil actuel.</span><span class="sxs-lookup"><span data-stu-id="de7b0-121">Returns a value indicating whether DVD codecs are enabled on the current device.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de7b0-122"><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-122"><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-123">Désactive la fonctionnalité de dédoublement de fenêtre pour le processus de l’interface graphique utilisateur appelant.</span><span class="sxs-lookup"><span data-stu-id="de7b0-123">Disables the window ghosting feature for the calling GUI process.</span></span> <span data-ttu-id="de7b0-124">Le dédoublement de fenêtre est une fonctionnalité du gestionnaire Windows qui permet à l’utilisateur de réduire, de déplacer ou de fermer la fenêtre principale d’une application qui ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="de7b0-124">Window ghosting is a Windows Manager feature that lets the user minimize, move, or close the main window of an application that is not responding.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7b0-125"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-125"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-126">Retourne la liste des propriétés de tous les codecs multimédias installés sur le système qui répondent aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="de7b0-126">Returns a list of properties for all media codecs installed on the system that meet the specified requirements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de7b0-127"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-127"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-128">Crée une fabrique de communication pour l’inscription d’une extension de média.</span><span class="sxs-lookup"><span data-stu-id="de7b0-128">Creates a communication factory for registering a media extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7b0-129"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-129"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-130">Crée une instance d’une classe dans un package d’application.</span><span class="sxs-lookup"><span data-stu-id="de7b0-130">Creates an instance of a class in an application package.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de7b0-131"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-131"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-132">Obtient une valeur indiquant si le comportement du média associé au GUID spécifié est activé.</span><span class="sxs-lookup"><span data-stu-id="de7b0-132">Gets a value indicating whether the media behavior associated with the specified GUID is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7b0-133"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-133"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-134">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="de7b0-134">Deprecated.</span></span> <span data-ttu-id="de7b0-135">Cette fonction est utilisée pour fermer le handle spécifié.</span><span class="sxs-lookup"><span data-stu-id="de7b0-135">This function is used to close the specified handle.</span></span> <span data-ttu-id="de7b0-136"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> est remplacé par <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="de7b0-136"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> is superseded by <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de7b0-137"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-137"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-138">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="de7b0-138">Deprecated.</span></span> <span data-ttu-id="de7b0-139">Génère des descripteurs pour la ou les mémoires tampons fournies et transmet les données non typées au pilote de périphérique associé au descripteur de fichier.</span><span class="sxs-lookup"><span data-stu-id="de7b0-139">Builds descriptors for the supplied buffer(s) and passes the untyped data to the device driver associated with the file handle.</span></span> <span data-ttu-id="de7b0-140"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> est remplacé par <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.</span><span class="sxs-lookup"><span data-stu-id="de7b0-140"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> is superseded by <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7b0-141"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-141"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-142">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="de7b0-142">Deprecated.</span></span> <span data-ttu-id="de7b0-143">Attend que l’objet spécifié atteigne un état de <code>signaled</code> .</span><span class="sxs-lookup"><span data-stu-id="de7b0-143">Waits until the specified object attains a state of <code>signaled</code>.</span></span> <span data-ttu-id="de7b0-144"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> est remplacé par <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.</span><span class="sxs-lookup"><span data-stu-id="de7b0-144"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> is superseded by <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de7b0-145"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-145"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-146">Convertit la chaîne source ANSI spécifiée en chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="de7b0-146">Converts the specified ANSI source string into a Unicode string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7b0-147"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-147"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-148">Convertit une chaîne de caractères en entier.</span><span class="sxs-lookup"><span data-stu-id="de7b0-148">Converts a character string to an integer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de7b0-149"><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-149"><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-150">Initialise la mémoire tampon fournie avec une représentation sous forme de chaîne du SID de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="de7b0-150">Initializes the supplied buffer with a string representation of the SID for the current user.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7b0-151"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-151"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-152">Libère la mémoire tampon de chaîne allouée par <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de7b0-152">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de7b0-153"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-153"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-154">Libère la mémoire tampon de chaîne allouée par <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de7b0-154">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7b0-155"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-155"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-156">Libère la mémoire tampon de chaîne allouée par <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> ou par <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>.</span><span class="sxs-lookup"><span data-stu-id="de7b0-156">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> or by <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de7b0-157"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-157"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-158">Initialise une chaîne comptée.</span><span class="sxs-lookup"><span data-stu-id="de7b0-158">Initializes a counted string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7b0-159"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-159"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-160">Initialise une chaîne Unicode comptée.</span><span class="sxs-lookup"><span data-stu-id="de7b0-160">Initializes a counted Unicode string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de7b0-161"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-161"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-162">Convertit la chaîne source Unicode spécifiée en chaîne ANSI.</span><span class="sxs-lookup"><span data-stu-id="de7b0-162">Converts the specified Unicode source string into an ANSI string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7b0-163"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-163"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-164">Cette fonction convertit la chaîne source Unicode spécifiée en une chaîne OEM.</span><span class="sxs-lookup"><span data-stu-id="de7b0-164">This functions converts the specified Unicode source string into an OEM string.</span></span> <span data-ttu-id="de7b0-165">La traduction est effectuée par rapport à la page de codes OEM (OCP).</span><span class="sxs-lookup"><span data-stu-id="de7b0-165">The translation is done with respect to the OEM code page (OCP).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de7b0-166"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-166"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-167">Détermine le nombre d’octets nécessaires pour représenter une chaîne Unicode sous la forme d’une chaîne ANSI.</span><span class="sxs-lookup"><span data-stu-id="de7b0-167">Determines how many bytes are needed to represent a Unicode string as an ANSI string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7b0-168"><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-168"><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-169">La fonction <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> traduit la chaîne Unicode spécifiée en une nouvelle chaîne de caractères, à l’aide de la page de codes UTF-8 (Unicode Transformation Format) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="de7b0-169">The <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> function translates the specified Unicode string into a new character string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de7b0-170"><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-170"><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-171">La fonction <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> traduit la chaîne source spécifiée en chaîne Unicode, à l’aide de la page de codes UTF-8.</span><span class="sxs-lookup"><span data-stu-id="de7b0-171">The <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> function translates the specified source string into a Unicode string, using the UTF-8 code page.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7b0-172"><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-172"><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-173">Spécifie une action ou un traitement pour l’éditeur de méthode d’entrée (IME) via une sous-fonction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="de7b0-173">Specifies an action or processing for the Input Method Editor (IME) through a specified subfunction.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="de7b0-174">Cette fonction est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="de7b0-174">This function is obsolete and should not be used.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de7b0-175"><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></span><span class="sxs-lookup"><span data-stu-id="de7b0-175"><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></span></span></td>
<td><span data-ttu-id="de7b0-176">Active ou désactive temporairement un IME et, en même temps, active ou désactive l’affichage de toutes les fenêtres détenues par l’IME.</span><span class="sxs-lookup"><span data-stu-id="de7b0-176">Temporarily enables or disables an IME and, at the same time, turns on or off the display of all windows owned by the IME.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="de7b0-177">Cette fonction est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="de7b0-177">This function is obsolete and should not be used.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a><span data-ttu-id="de7b0-178">Structures</span><span class="sxs-lookup"><span data-stu-id="de7b0-178">Structures</span></span>



| <span data-ttu-id="de7b0-179">Rubrique</span><span class="sxs-lookup"><span data-stu-id="de7b0-179">Topic</span></span>                                 | <span data-ttu-id="de7b0-180">Contenu</span><span class="sxs-lookup"><span data-stu-id="de7b0-180">Contents</span></span>                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de7b0-181">**IMESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="de7b0-181">**IMESTRUCT**</span></span>](/windows/win32/api/ime/ns-ime-imestruct) | <span data-ttu-id="de7b0-182">Utilisé par [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) pour spécifier la sous-fonction à exécuter dans le message IME et ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="de7b0-182">Used by [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) to specify the subfunction to be executed in the IME message and its parameters.</span></span> <span data-ttu-id="de7b0-183">Cette structure est également utilisée pour recevoir des valeurs de retour de ces sous-fonctions.</span><span class="sxs-lookup"><span data-stu-id="de7b0-183">This structure is also used to receive return values from those subfunctions.</span></span><br/> |
| [<span data-ttu-id="de7b0-184">**CHAÎNE**</span><span class="sxs-lookup"><span data-stu-id="de7b0-184">**STRING**</span></span>](/windows/desktop/api/Winternl/ns-winternl-string)       | <span data-ttu-id="de7b0-185">Cette structure est utilisée avec la fonction [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) .</span><span class="sxs-lookup"><span data-stu-id="de7b0-185">This structure is used with the [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) function.</span></span> <br/>                                                                                                              |



 

### <a name="compiler-routines"></a><span data-ttu-id="de7b0-186">Routines du compilateur</span><span class="sxs-lookup"><span data-stu-id="de7b0-186">Compiler Routines</span></span>



| <span data-ttu-id="de7b0-187">Rubrique</span><span class="sxs-lookup"><span data-stu-id="de7b0-187">Topic</span></span>                                                             | <span data-ttu-id="de7b0-188">Contenu</span><span class="sxs-lookup"><span data-stu-id="de7b0-188">Contents</span></span>                                                                                                     |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de7b0-189">**\_\_\_Routine de gestionnaire spécifique à C \_**</span><span class="sxs-lookup"><span data-stu-id="de7b0-189">**\_\_C\_specific\_handler Routine**</span></span>](--c-specific-handler2.md) | <span data-ttu-id="de7b0-190">Le [**\_ \_ \_ \_ gestionnaire spécifique à c**](--c-specific-handler2.md) est une routine d’assistance pour le compilateur c.</span><span class="sxs-lookup"><span data-stu-id="de7b0-190">[**\_\_C\_specific\_handler**](--c-specific-handler2.md) is a helper routine for the C compiler.</span></span><br/> |
| [<span data-ttu-id="de7b0-191">\_Routine alldiv</span><span class="sxs-lookup"><span data-stu-id="de7b0-191">\_alldiv Routine</span></span>](-win32-alldiv.md)                             | <span data-ttu-id="de7b0-192">la [ \_ routine alldiv](-win32-alldiv.md) est une routine d’assistance pour le compilateur C.</span><span class="sxs-lookup"><span data-stu-id="de7b0-192">[\_alldiv Routine](-win32-alldiv.md) is a helper routine for the C compiler.</span></span><br/>                     |
| [<span data-ttu-id="de7b0-193">\_allmul</span><span class="sxs-lookup"><span data-stu-id="de7b0-193">\_allmul</span></span>](-win32-allmul.md) | <span data-ttu-id="de7b0-194">Multiplie deux **LongLong** ou **ULONGLONG**.</span><span class="sxs-lookup"><span data-stu-id="de7b0-194">Multiplies two **LONGLONG** or **ULONGLONG**.</span></span> |
| [<span data-ttu-id="de7b0-195">\_aulldiv</span><span class="sxs-lookup"><span data-stu-id="de7b0-195">\_aulldiv</span></span>](-win32-aulldiv.md) | <span data-ttu-id="de7b0-196">Divise deux entiers **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="de7b0-196">Divides two **ULONGLONG** integers.</span></span> |
| [<span data-ttu-id="de7b0-197">\_Routine chkstk</span><span class="sxs-lookup"><span data-stu-id="de7b0-197">\_chkstk Routine</span></span>](-win32-chkstk.md)                             | <span data-ttu-id="de7b0-198">la [ \_ routine chkstk](-win32-chkstk.md) est une routine d’assistance pour le compilateur C.</span><span class="sxs-lookup"><span data-stu-id="de7b0-198">[\_chkstk Routine](-win32-chkstk.md) is a helper routine for the C compiler.</span></span><br/>                     |
