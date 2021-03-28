---
description: Récupère un paramètre d’interpréteur de commandes global.
ms.assetid: 3E8C7C6A-5696-4756-B4BF-902FA2420AE9
title: Shell. GetSetting, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: df87c0c99129a8ececa3c25321a192e25c71c07e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865266"
---
# <a name="shellgetsetting-method"></a><span data-ttu-id="af8bd-103">Shell. GetSetting, méthode</span><span class="sxs-lookup"><span data-stu-id="af8bd-103">Shell.GetSetting method</span></span>

<span data-ttu-id="af8bd-104">Récupère un paramètre d’interpréteur de commandes global.</span><span class="sxs-lookup"><span data-stu-id="af8bd-104">Retrieves a global Shell setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="af8bd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af8bd-105">Syntax</span></span>


```JScript
retVal = Shell.GetSetting(
  lSetting
)
```


```VB

Shell.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a><span data-ttu-id="af8bd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af8bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af8bd-107">*lSetting* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af8bd-107">*lSetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af8bd-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="af8bd-108">Type: **long**</span></span>

<span data-ttu-id="af8bd-109">Valeur qui spécifie le paramètre d’interpréteur de commandes en cours à récupérer.</span><span class="sxs-lookup"><span data-stu-id="af8bd-109">A value that specifies the current Shell setting to retrieve.</span></span> <span data-ttu-id="af8bd-110">Un seul paramètre peut être récupéré dans chaque appel.</span><span class="sxs-lookup"><span data-stu-id="af8bd-110">Only one setting can be retrieved in each call.</span></span> <span data-ttu-id="af8bd-111">Les valeurs suivantes sont reconnues par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="af8bd-111">The following values are recognized by this method.</span></span>

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span data-ttu-id="af8bd-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ AUTOCHECKSELECT** (0x00800000)</span><span class="sxs-lookup"><span data-stu-id="af8bd-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF\_AUTOCHECKSELECT** (0x00800000)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-113">**Windows Vista et versions ultérieures**.</span><span class="sxs-lookup"><span data-stu-id="af8bd-113">**Windows Vista and later**.</span></span> <span data-ttu-id="af8bd-114">État de l’option **utiliser les cases à cocher pour sélectionner les éléments** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-114">The state of the **Use check boxes to select items** option.</span></span> <span data-ttu-id="af8bd-115">Cette option est activée automatiquement quand un appareil d’entrée Pen est configuré sur le système.</span><span class="sxs-lookup"><span data-stu-id="af8bd-115">This option is enabled automatically when the system has a pen input device configured.</span></span>

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span data-ttu-id="af8bd-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ DESKTOPHTML** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="af8bd-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-117">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="af8bd-117">Not used.</span></span>

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span data-ttu-id="af8bd-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ DONTPRETTYPATH** (0x00000800)</span><span class="sxs-lookup"><span data-stu-id="af8bd-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF\_DONTPRETTYPATH** (0x00000800)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-119">L’état de l’option **autoriser tous les noms en majuscules** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-119">The state of the **Allow all uppercase names** option.</span></span> <span data-ttu-id="af8bd-120">À compter de Windows Vista, cette option de dossier n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="af8bd-120">As of Windows Vista, this folder option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span data-ttu-id="af8bd-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ DOUBLECLICKINWEBVIEW** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="af8bd-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-122">État du **double-clic pour ouvrir une option d’élément (simple clic à sélectionner)** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-122">The state of the **Double-click to open an item (single-click to select)** option.</span></span>

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span data-ttu-id="af8bd-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF \_ FILTRE** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="af8bd-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF\_FILTER** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-124">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="af8bd-124">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span data-ttu-id="af8bd-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ HIDDENFILEEXTS** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="af8bd-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF\_HIDDENFILEEXTS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-126">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="af8bd-126">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span data-ttu-id="af8bd-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_ HIDEICONS** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="af8bd-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF\_HIDEICONS** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-128">État de l’affichage des icônes dans le mode liste de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="af8bd-128">The state of icon display in the Windows Explorer list view.</span></span> <span data-ttu-id="af8bd-129">Si cette option est active, aucune icône n’est affichée en mode liste.</span><span class="sxs-lookup"><span data-stu-id="af8bd-129">If this option is active, no icons are displayed in the list view.</span></span>

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span data-ttu-id="af8bd-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ ICONSONLY** (0x01000000)</span><span class="sxs-lookup"><span data-stu-id="af8bd-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF\_ICONSONLY** (0x01000000)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-131">**Windows Vista et versions ultérieures**.</span><span class="sxs-lookup"><span data-stu-id="af8bd-131">**Windows Vista and later**.</span></span> <span data-ttu-id="af8bd-132">L’état du nom d’affichage est affiché dans l’affichage de liste de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="af8bd-132">The state of display name display in the Windows Explorer list view.</span></span> <span data-ttu-id="af8bd-133">Si cette option est active, les icônes sont affichées en mode liste, mais pas les noms d’affichage.</span><span class="sxs-lookup"><span data-stu-id="af8bd-133">If this option is active, icons are displayed in the list view, but display names are not.</span></span>

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span data-ttu-id="af8bd-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ MAPNETDRVBUTTON** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="af8bd-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF\_MAPNETDRVBUTTON** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-135">État du **bouton afficher le lecteur réseau dans la barre d’outils** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-135">The state of the **Show map network drive button in toolbar** option.</span></span> <span data-ttu-id="af8bd-136">À compter de Windows Vista, cette option n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="af8bd-136">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span data-ttu-id="af8bd-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ NOCONFIRMRECYCLE** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="af8bd-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF\_NOCONFIRMRECYCLE** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-138">État de l’option d’affichage de la **boîte de dialogue de confirmation de suppression** de la corbeille.</span><span class="sxs-lookup"><span data-stu-id="af8bd-138">The state of the Recycle Bin's **Display delete confirmation dialog** option.</span></span>

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span data-ttu-id="af8bd-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ NONETCRAWLING** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="af8bd-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF\_NONETCRAWLING** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-140">État de l’option **Rechercher automatiquement les dossiers et imprimantes réseau** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-140">The state of the **Automatically search for network folders and printers** option.</span></span> <span data-ttu-id="af8bd-141">À compter de Windows Vista, cette option n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="af8bd-141">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span data-ttu-id="af8bd-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ SEPPROCESS** (0x00080000)</span><span class="sxs-lookup"><span data-stu-id="af8bd-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF\_SEPPROCESS** (0x00080000)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-143">État du dossier de **lancement Windows dans une option de processus distincte** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-143">The state of the **Launch folder windows in a separate process** option.</span></span>

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span data-ttu-id="af8bd-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ SERVERADMINUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="af8bd-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF\_SERVERADMINUI** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-145">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="af8bd-145">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span data-ttu-id="af8bd-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ SHOWALLOBJECTS** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="af8bd-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-147">État de l’option **fichiers et dossiers cachés** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-147">The state of the **Hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span data-ttu-id="af8bd-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ SHOWATTRIBCOL** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="af8bd-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF\_SHOWATTRIBCOL** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-149">État de l’option **afficher les attributs de fichier en mode Détails** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-149">The state of the **Show File Attributes in Detail View** option.</span></span> <span data-ttu-id="af8bd-150">À compter de Windows Vista, cette option n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="af8bd-150">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span data-ttu-id="af8bd-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ SHOWCOMPCOLOR** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="af8bd-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-152">État de l’option **afficher les fichiers NTFS chiffrés ou compressés en couleur** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-152">The state of the **Show encrypted or compressed NTFS files in color** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span data-ttu-id="af8bd-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_ SHOWEXTENSIONS** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="af8bd-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-154">État de l’option **Masquer les extensions pour les types de fichiers connus** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-154">The state of the **Hide extensions for known file types** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span data-ttu-id="af8bd-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ SHOWINFOTIP** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="af8bd-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF\_SHOWINFOTIP** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-156">État de l’option **afficher la description contextuelle pour les éléments de dossier et de bureau** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-156">The state of the **Show pop-up description for folder and desktop items** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span data-ttu-id="af8bd-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ SHOWSTARTPAGE** (0x00400000)</span><span class="sxs-lookup"><span data-stu-id="af8bd-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF\_SHOWSTARTPAGE** (0x00400000)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-158">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="af8bd-158">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span data-ttu-id="af8bd-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ SHOWSUPERHIDDEN** (0x00040000)</span><span class="sxs-lookup"><span data-stu-id="af8bd-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF\_SHOWSUPERHIDDEN** (0x00040000)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-160">État de l’option **Masquer les fichiers protégés du système d’exploitation** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-160">The state of the **Hide protected operating system files** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span data-ttu-id="af8bd-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_ SHOWSYSFILES** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="af8bd-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-162">État de l’option **fichiers et dossiers cachés** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-162">The state of the **Hidden files and folders** option.</span></span> <span data-ttu-id="af8bd-163">Dans Windows Vista et versions ultérieures, cette valeur est équivalente à SSF \_ SHOWALLOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="af8bd-163">In Windows Vista and later, this is equivalent to SSF\_SHOWALLOBJECTS.</span></span> <span data-ttu-id="af8bd-164">Dans les versions de Windows antérieures à Windows Vista, cette valeur faisait état de l’option **ne pas afficher les fichiers et les dossiers masqués** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-164">In versions of Windows before Windows Vista, this value referred to the state of the **Do not show hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span data-ttu-id="af8bd-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ SHOWTYPEOVERLAY** (0x02000000)</span><span class="sxs-lookup"><span data-stu-id="af8bd-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF\_SHOWTYPEOVERLAY** (0x02000000)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-166">**Windows Vista et versions ultérieures**.</span><span class="sxs-lookup"><span data-stu-id="af8bd-166">**Windows Vista and later**.</span></span> <span data-ttu-id="af8bd-167">État de l' **icône Afficher le fichier sur les miniatures** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-167">The state of the **Display file icon on thumbnails** option.</span></span> <span data-ttu-id="af8bd-168">Si cette option est active, une superposition de type de fichier est appliquée lorsqu’un fichier fournit une représentation miniature.</span><span class="sxs-lookup"><span data-stu-id="af8bd-168">If this option is active, a file type overlay is applied when a file supplies a thumbnail representation.</span></span>

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span data-ttu-id="af8bd-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ SORTCOLUMNS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="af8bd-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF\_SORTCOLUMNS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-170">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="af8bd-170">Not used.</span></span>

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span data-ttu-id="af8bd-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ STARTPANELON** (0x00200000)</span><span class="sxs-lookup"><span data-stu-id="af8bd-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF\_STARTPANELON** (0x00200000)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-172">État de l’option d’affichage de Windows XP, qui permet de sélectionner le style Windows XP et le style classique.</span><span class="sxs-lookup"><span data-stu-id="af8bd-172">The state of the Windows XP display option, which selects between the Windows XP style and the classic style.</span></span> <span data-ttu-id="af8bd-173">À compter de Windows Vista, cette option n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="af8bd-173">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span data-ttu-id="af8bd-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_ VUE WebView** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="af8bd-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF\_WEBVIEW** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-175">État de l' **affichage comme une option d’affichage Web**.</span><span class="sxs-lookup"><span data-stu-id="af8bd-175">The state of the **Display as a web view option**.</span></span> <span data-ttu-id="af8bd-176">À compter de Windows Vista, cette option n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="af8bd-176">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span data-ttu-id="af8bd-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC** (0x00000400)</span><span class="sxs-lookup"><span data-stu-id="af8bd-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF\_WIN95CLASSIC** (0x00000400)</span></span>


</dt> <dd>

<span data-ttu-id="af8bd-178">État de l’option de **style classique** .</span><span class="sxs-lookup"><span data-stu-id="af8bd-178">The state of the **Classic Style** option.</span></span> <span data-ttu-id="af8bd-179">À compter de Windows Vista, cette option n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="af8bd-179">As of Windows Vista, this option is no longer available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af8bd-180">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af8bd-180">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="af8bd-181">JScript</span><span class="sxs-lookup"><span data-stu-id="af8bd-181">JScript</span></span>

<span data-ttu-id="af8bd-182">Type : \**Variant \_ bool \** _</span><span class="sxs-lookup"><span data-stu-id="af8bd-182">Type: \**VARIANT\_BOOL\** _</span></span>

<span data-ttu-id="af8bd-183">A la valeur _ *true*\* si le paramètre existe ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="af8bd-183">Set to _ *true*\* if the setting exists; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="af8bd-184">VB</span><span class="sxs-lookup"><span data-stu-id="af8bd-184">VB</span></span>

<span data-ttu-id="af8bd-185">Type : \**Variant \_ bool \** _</span><span class="sxs-lookup"><span data-stu-id="af8bd-185">Type: \**VARIANT\_BOOL\** _</span></span>

<span data-ttu-id="af8bd-186">A la valeur _ *true*\* si le paramètre existe ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="af8bd-186">Set to _ *true*\* if the setting exists; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="af8bd-187">Exemples</span><span class="sxs-lookup"><span data-stu-id="af8bd-187">Examples</span></span>

<span data-ttu-id="af8bd-188">Les exemples suivants illustrent l’utilisation de **GetSetting** pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="af8bd-188">The following examples show the use of **GetSetting** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="af8bd-189">Langage</span><span class="sxs-lookup"><span data-stu-id="af8bd-189">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnIShellDispatch4GetSettingJ()
    {
        var objIShellDispatch4 = new ActiveXObject("Shell.Application");
        var vReturn;
        var ssfSHOWALLOBJECTS = 1;

        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS);
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="af8bd-190">VBScript</span><span class="sxs-lookup"><span data-stu-id="af8bd-190">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellDispatch4GetSettingVB()
        dim objIShellDispatch4
        
        set objIShellDispatch4 = CreateObject("Shell.Application")
        if (not objIShellDispatch4 is nothing) then
            dim vReturn
            dim ssfSHOWALLOBJECTS
            
            ssfSHOWALLOBJECTS = 1
            vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
            alert(vReturn)
        end if
        set objIShellDispatch4 = nothing
    end function
```



<span data-ttu-id="af8bd-191">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="af8bd-191">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4GetSetting()
    Dim objIShellDispatch4 As Shell
    
    Set objIShellDispatch4 = New Shell
    If (Not objIShellDispatch4 Is Nothing) Then
        Dim vReturn As Variant
        Dim ssfSHOWALLOBJECTS As Long
        
        ssfSHOWALLOBJECTS = 1
        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
        Debug.Print vReturn
    End If
    Set objIShellDispatch4 = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="af8bd-192">Spécifications</span><span class="sxs-lookup"><span data-stu-id="af8bd-192">Requirements</span></span>



| <span data-ttu-id="af8bd-193">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af8bd-193">Requirement</span></span> | <span data-ttu-id="af8bd-194">Valeur</span><span class="sxs-lookup"><span data-stu-id="af8bd-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af8bd-195">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af8bd-195">Minimum supported client</span></span><br/> | <span data-ttu-id="af8bd-196">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af8bd-196">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="af8bd-197">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af8bd-197">Minimum supported server</span></span><br/> | <span data-ttu-id="af8bd-198">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af8bd-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="af8bd-199">En-tête</span><span class="sxs-lookup"><span data-stu-id="af8bd-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="af8bd-200"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="af8bd-200"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="af8bd-201">MIDL</span><span class="sxs-lookup"><span data-stu-id="af8bd-201">IDL</span></span><br/>                      | <dl> <span data-ttu-id="af8bd-202"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="af8bd-202"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="af8bd-203">DLL</span><span class="sxs-lookup"><span data-stu-id="af8bd-203">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af8bd-204"><dt>Shell32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="af8bd-204"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




