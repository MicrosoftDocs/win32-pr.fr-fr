---
title: Utilisation de structures dans WCS 1.0
description: La plupart des structures utilisées par WCS 1,0 sont très simples et nécessitent peu d’explications. Elles sont documentées dans la section de référence du WCS 1,0 structures d’intitulé.
ms.assetid: 8d3682e2-38fd-4a33-b386-ab0716bb6972
keywords:
- Système de couleurs Windows (WCS), structures
- WCS (système de couleurs Windows), structures
- gestion des couleurs des images, structures
- gestion des couleurs, structures
- couleurs, structures
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d6e434ccfa6d96aa815f0c1997dc7f34178a32
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106531264"
---
# <a name="using-structures-in-wcs-10"></a><span data-ttu-id="4f543-109">Utilisation de structures dans WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="4f543-109">Using Structures in WCS 1.0</span></span>

<span data-ttu-id="4f543-110">La plupart des structures utilisées par WCS 1,0 sont très simples et nécessitent peu d’explications.</span><span class="sxs-lookup"><span data-stu-id="4f543-110">Most of the structures used by WCS 1.0 are very straightforward and require little explanation.</span></span> <span data-ttu-id="4f543-111">Elles sont documentées dans la section de référence du WCS 1,0 [structures](structures.md)d’intitulé.</span><span class="sxs-lookup"><span data-stu-id="4f543-111">They are documented in the WCS 1.0 Reference section entitled [Structures](structures.md).</span></span>

<span data-ttu-id="4f543-112">Les exceptions sont la structure [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) utilisée par la fonction [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) , et les structures Windows suivantes définies dans WinGDI. h :</span><span class="sxs-lookup"><span data-stu-id="4f543-112">Exceptions are the [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) structure used by the [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) function, and the following Windows structures defined in Wingdi.h:</span></span>

-   [<span data-ttu-id="4f543-113">BITMAPV5HEADER</span><span class="sxs-lookup"><span data-stu-id="4f543-113">BITMAPV5HEADER</span></span>](#windows-bitmap-header-structures)
-   [<span data-ttu-id="4f543-114">**LOGCOLORSPACE**</span><span class="sxs-lookup"><span data-stu-id="4f543-114">**LOGCOLORSPACE**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)
-   [<span data-ttu-id="4f543-115">**CIEXYZ**</span><span class="sxs-lookup"><span data-stu-id="4f543-115">**CIEXYZ**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-tagciexyz)
-   [<span data-ttu-id="4f543-116">**CIEXYZTRIPLE**</span><span class="sxs-lookup"><span data-stu-id="4f543-116">**CIEXYZTRIPLE**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-tagicexyztriple)

<span data-ttu-id="4f543-117">Les rubriques suivantes sont traitées de façon plus longue :</span><span class="sxs-lookup"><span data-stu-id="4f543-117">The following topics are discussed at greater length:</span></span>

-   [<span data-ttu-id="4f543-118">Structures d’en-tête bitmap Windows</span><span class="sxs-lookup"><span data-stu-id="4f543-118">Windows Bitmap Header Structures</span></span>](#windows-bitmap-header-structures)
-   [<span data-ttu-id="4f543-119">Différences entre les en-têtes V4 et v5</span><span class="sxs-lookup"><span data-stu-id="4f543-119">Differences Between V4 and V5 Headers</span></span>](#differences-between-v4-and-v5-headers)
-   [<span data-ttu-id="4f543-120">Bitmap.exe : utilitaire Command-Line pour la conversion d’en-têtes bitmap</span><span class="sxs-lookup"><span data-stu-id="4f543-120">Bitmap.exe: a Command-Line Utility for Converting Bitmap Headers</span></span>](#bitmapexe-a-command-line-utility-for-converting-bitmap-headers)

## <a name="windows-bitmap-header-structures"></a><span data-ttu-id="4f543-121">Structures d’en-tête bitmap Windows</span><span class="sxs-lookup"><span data-stu-id="4f543-121">Windows Bitmap Header Structures</span></span>

<span data-ttu-id="4f543-122">WCS 1,0 permet de lier ou d’incorporer les profils de couleurs ICC dans des bitmaps indépendantes du périphérique (DIB).</span><span class="sxs-lookup"><span data-stu-id="4f543-122">WCS 1.0 allows ICC color profiles to be linked or embedded in device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="4f543-123">Cela permet de caractériser les couleurs DIB de manière plus précise que si vous utilisiez WCS dans Windows 95.</span><span class="sxs-lookup"><span data-stu-id="4f543-123">This allows DIB colors to be characterized more accurately than was possible using WCS in Windows 95.</span></span> <span data-ttu-id="4f543-124">[BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , la nouvelle structure d’en-tête bitmap, est définie dans WinGDI. h dans la version de Windows 98.</span><span class="sxs-lookup"><span data-stu-id="4f543-124">[BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , the new bitmap header structure, is defined in Wingdi.h in the release of Windows 98.</span></span> <span data-ttu-id="4f543-125">À des fins de développement, il est également inclus dans le fichier ICM. h avec ce guide de référence du programmeur.</span><span class="sxs-lookup"><span data-stu-id="4f543-125">For development purposes, it is also included in the file Icm.h with this Programmer's Reference.</span></span> <span data-ttu-id="4f543-126">La structure **BITMAPV5HEADER** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="4f543-126">The **BITMAPV5HEADER** structure is as follows:</span></span>


```C++
typedef struct {
    DWORD        bV5Size;
    LONG         bV5Width;
    LONG         bV5Height;
    WORD         bV5Planes;
    WORD         bV5BitCount;
    DWORD        bV5Compression;
    DWORD        bV5SizeImage;
    LONG         bV5XPelsPerMeter;
    LONG         bV5YPelsPerMeter;
    DWORD        bV5ClrUsed;
    DWORD        bV5ClrImportant;
    DWORD        bV5RedMask;
    DWORD        bV5GreenMask;
    DWORD        bV5BlueMask;
    DWORD        bV5AlphaMask;
    DWORD        bV5CSType;
    CIEXYZTRIPLE bV5Endpoints;
    DWORD        bV5GammaRed;
    DWORD        bV5GammaGreen;
    DWORD        bV5GammaBlue;
    DWORD        bV5Intent;         // Rendering intent for bitmap 
    DWORD        bV5ProfileData;    // Offset to profile data 
    DWORD        bV5ProfileSize;    // Size of embedded profile data 
    DWORD        bV5Reserved;       // Should be zero 
} BITMAPV5HEADER, FAR *LPBITMAPV5HEADER, *PBITMAPV5HEADER;
```



<span data-ttu-id="4f543-127">Le **bV5CSType** membre peut avoir le profil des valeurs \_ incorporé ou le profil \_ lié pour spécifier si un profil est incorporé ou lié au dib.</span><span class="sxs-lookup"><span data-stu-id="4f543-127">The member **bV5CSType** can have the values PROFILE\_EMBEDDED or PROFILE\_LINKED to specify whether a profile is embedded or linked with the DIB.</span></span> <span data-ttu-id="4f543-128">Le membre **bV5ProfileData** est le décalage, en octets, entre le début de la structure **BITMAPV5HEADER** et le début des données de profil.</span><span class="sxs-lookup"><span data-stu-id="4f543-128">The member **bV5ProfileData** is the offset in bytes from the beginning of the **BITMAPV5HEADER** structure to the start of the profile data.</span></span> <span data-ttu-id="4f543-129">Si le profil est incorporé, les données de profil sont le profil réel et, s’il est lié, les données de profil sont le nom de fichier se terminant par un caractère null du profil.</span><span class="sxs-lookup"><span data-stu-id="4f543-129">If the profile is embedded, profile data is the actual profile, and if it is linked, the profile data is the null-terminated file name of the profile.</span></span> <span data-ttu-id="4f543-130">Il ne peut pas s’agir d’une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="4f543-130">This cannot be a Unicode string.</span></span> <span data-ttu-id="4f543-131">Elle doit être composée exclusivement de caractères à partir du jeu de caractères Windows (page de codes 1252).</span><span class="sxs-lookup"><span data-stu-id="4f543-131">It must be composed exclusively of characters from the Windows character set (code page 1252).</span></span>

<span data-ttu-id="4f543-132">Lorsqu’un DIB est chargé en mémoire, les données de profil (le cas échéant) doivent suivre la table des couleurs, et **bV5ProfileData** doit donner le décalage des données de profil à partir du début de la structure **BITMAPV5HEADER** .</span><span class="sxs-lookup"><span data-stu-id="4f543-132">When a DIB is loaded into memory, the profile data (if present) should follow the color table, and **bV5ProfileData** should give the offset of the profile data from the beginning of the **BITMAPV5HEADER** structure.</span></span> <span data-ttu-id="4f543-133">La valeur de ce membre sera maintenant différente, car les bits de la bitmap ne suivent pas la table des couleurs en mémoire.</span><span class="sxs-lookup"><span data-stu-id="4f543-133">The value of this member will be different now, as the bitmap bits do not follow the color table in memory.</span></span> <span data-ttu-id="4f543-134">Les applications doivent modifier le membre **bV5ProfileData** après le chargement du DIB dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="4f543-134">Applications should modify the **bV5ProfileData** member after loading the DIB into memory.</span></span>

<span data-ttu-id="4f543-135">Pour les fichiers DIB compactés, les données de profil doivent suivre les bits de bitmap similaires au format de fichier.</span><span class="sxs-lookup"><span data-stu-id="4f543-135">For packed DIBs, the profile data should follow the bitmap bits similar to the file format.</span></span> <span data-ttu-id="4f543-136">Le membre **bV5ProfileData** doit toujours fournir le décalage des données de profil à partir du début de la structure **BITMAPV5HEADER** .</span><span class="sxs-lookup"><span data-stu-id="4f543-136">The **bV5ProfileData** member should still give the offset of the profile data from the beginning of the **BITMAPV5HEADER** structure.</span></span>

<span data-ttu-id="4f543-137">Les applications doivent accéder aux données de profil uniquement quand **bV5Size**  ==  **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** est un profil \_ incorporé ou un profil \_ lié.</span><span class="sxs-lookup"><span data-stu-id="4f543-137">Applications should access the profile data only when **bV5Size** == **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** is PROFILE\_EMBEDDED or PROFILE\_LINKED.</span></span>

<span data-ttu-id="4f543-138">Si un profil est lié, le chemin d’accès du profil peut être n’importe quel nom complet (y compris un chemin d’accès réseau) qui peut être ouvert à l’aide de la fonction **CreateFile** de Win32.</span><span class="sxs-lookup"><span data-stu-id="4f543-138">If a profile is linked, the path of the profile can be any fully qualified name (including a network path) that can be opened using the Win32 **CreateFile** function.</span></span>

## <a name="differences-between-v4-and-v5-headers"></a><span data-ttu-id="4f543-139">Différences entre les en-têtes V4 et v5</span><span class="sxs-lookup"><span data-stu-id="4f543-139">Differences Between V4 and V5 Headers</span></span>

<span data-ttu-id="4f543-140">Dans l’utilisation de la nouvelle structure bitmap, il est utile de reconnaître les différences de configuration des structures **BITMAPV4HEADER** et **BITMAPV5HEADER** :</span><span class="sxs-lookup"><span data-stu-id="4f543-140">In working with the new bitmap structure, it is useful to recognize differences in how **BITMAPV4HEADER** and **BITMAPV5HEADER** structures are set up:</span></span>



| <span data-ttu-id="4f543-141">En-tête v4</span><span class="sxs-lookup"><span data-stu-id="4f543-141">V4 Header</span></span>     | <span data-ttu-id="4f543-142">Signification</span><span class="sxs-lookup"><span data-stu-id="4f543-142">Meaning</span></span>                                                                                                                              |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f543-143">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="4f543-143">**bV4CSType**</span></span> | <span data-ttu-id="4f543-144">\_ \_ RGB étalonné.</span><span class="sxs-lookup"><span data-stu-id="4f543-144">LCS\_CALIBRATED\_RGB.</span></span> <span data-ttu-id="4f543-145">Cette valeur implique que les points de terminaison et les gammas sont fournis dans les champs appropriés.</span><span class="sxs-lookup"><span data-stu-id="4f543-145">This value implies that end points and gammas are given in the appropriate fields.</span></span> <span data-ttu-id="4f543-146">Des valeurs erronées provoquent des problèmes.</span><span class="sxs-lookup"><span data-stu-id="4f543-146">Bogus values cause trouble.</span></span> |
| <span data-ttu-id="4f543-147">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="4f543-147">**bV4CSType**</span></span> | <span data-ttu-id="4f543-148">SRGB de LCS \_ .</span><span class="sxs-lookup"><span data-stu-id="4f543-148">LCS\_sRGB.</span></span> <span data-ttu-id="4f543-149">Cette valeur implique que la bitmap se trouve dans l’espace de couleurs sRVB (gammas et points de terminaison ignorés).</span><span class="sxs-lookup"><span data-stu-id="4f543-149">This value implies that the bitmap is in sRGB color space (gammas and endpoints ignored).</span></span>                                 |
| <span data-ttu-id="4f543-150">**bV4CSType**</span><span class="sxs-lookup"><span data-stu-id="4f543-150">**bV4CSType**</span></span> | <span data-ttu-id="4f543-151">\_espace de \_ couleurs Windows LCS \_ .</span><span class="sxs-lookup"><span data-stu-id="4f543-151">LCS\_WINDOWS\_COLOR\_SPACE.</span></span> <span data-ttu-id="4f543-152">Cette valeur implique que la bitmap se trouve dans l’espace de couleurs Windows par défaut.</span><span class="sxs-lookup"><span data-stu-id="4f543-152">This value implies that the bitmap is in Windows default color space.</span></span>                                    |



 



| <span data-ttu-id="4f543-153">En-tête v5</span><span class="sxs-lookup"><span data-stu-id="4f543-153">V5 Header</span></span>     | <span data-ttu-id="4f543-154">Signification</span><span class="sxs-lookup"><span data-stu-id="4f543-154">Meaning</span></span>                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f543-155">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="4f543-155">**bV5CSType**</span></span> | <span data-ttu-id="4f543-156">\_ \_ RGB étalonné.</span><span class="sxs-lookup"><span data-stu-id="4f543-156">LCS\_CALIBRATED\_RGB.</span></span> <span data-ttu-id="4f543-157">Cette valeur implique que les points de terminaison et les gammas sont fournis dans les champs appropriés.</span><span class="sxs-lookup"><span data-stu-id="4f543-157">This value implies that end points and gammas are given in the appropriate fields.</span></span> <span data-ttu-id="4f543-158">Des valeurs erronées provoquent des problèmes.</span><span class="sxs-lookup"><span data-stu-id="4f543-158">Bogus values cause trouble.</span></span>                         |
| <span data-ttu-id="4f543-159">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="4f543-159">**bV5CSType**</span></span> | <span data-ttu-id="4f543-160">SRGB de LCS \_ .</span><span class="sxs-lookup"><span data-stu-id="4f543-160">LCS\_sRGB.</span></span> <span data-ttu-id="4f543-161">Cette valeur implique que la bitmap se trouve dans l’espace de couleurs sRVB (gammas et points de terminaison ignorés).</span><span class="sxs-lookup"><span data-stu-id="4f543-161">This value implies that the bitmap is in sRGB color space (gammas and endpoints ignored).</span></span>                                                         |
| <span data-ttu-id="4f543-162">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="4f543-162">**bV5CSType**</span></span> | <span data-ttu-id="4f543-163">Profil \_ incorporé.</span><span class="sxs-lookup"><span data-stu-id="4f543-163">PROFILE\_EMBEDDED.</span></span> <span data-ttu-id="4f543-164">Cette valeur implique que **bV5ProfileData** pointe vers une mémoire tampon qui contient le profil à utiliser (les valeurs gamma et les points de terminaison sont ignorés).</span><span class="sxs-lookup"><span data-stu-id="4f543-164">This value implies that **bV5ProfileData** points to a memory buffer that contains the profile to use (gammas and endpoints are ignored).</span></span> |
| <span data-ttu-id="4f543-165">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="4f543-165">**bV5CSType**</span></span> | <span data-ttu-id="4f543-166">Profil \_ lié.</span><span class="sxs-lookup"><span data-stu-id="4f543-166">PROFILE\_LINKED.</span></span> <span data-ttu-id="4f543-167">Cette valeur implique que **bV5ProfileData** pointe vers le nom de fichier du profil à utiliser (les valeurs gamma et les points de terminaison sont ignorés).</span><span class="sxs-lookup"><span data-stu-id="4f543-167">This value implies that **bV5ProfileData** points to the file name of the profile to use (gammas and endpoints are ignored).</span></span>                |
| <span data-ttu-id="4f543-168">**bV5CSType**</span><span class="sxs-lookup"><span data-stu-id="4f543-168">**bV5CSType**</span></span> | <span data-ttu-id="4f543-169">\_espace de \_ couleurs Windows LCS \_ .</span><span class="sxs-lookup"><span data-stu-id="4f543-169">LCS\_WINDOWS\_COLOR\_SPACE.</span></span> <span data-ttu-id="4f543-170">Cette valeur implique que la bitmap se trouve dans l’espace de couleurs Windows par défaut.</span><span class="sxs-lookup"><span data-stu-id="4f543-170">This value implies that the bitmap is in Windows default color space.</span></span>                                                            |



 

<span data-ttu-id="4f543-171">Pour convertir les bitmaps plus anciennes vers et à partir de la nouvelle structure **BITMAPV5HEADER** , un fichier utilitaire de conversion de ligne de commande nommé Bitmap.exe est inclus dans le Guide de référence du programmeur WCS 1,0.</span><span class="sxs-lookup"><span data-stu-id="4f543-171">In order to convert older bitmaps to and from the new **BITMAPV5HEADER** structure, a command-line conversion utility file named Bitmap.exe is included in the WCS 1.0 Programmer's Reference.</span></span>

## <a name="bitmapexe-a-command-line-utility-for-converting-bitmap-headers"></a><span data-ttu-id="4f543-172">BitMap.exe : utilitaire Command-Line pour la conversion d’en-têtes bitmap</span><span class="sxs-lookup"><span data-stu-id="4f543-172">BitMap.exe: a Command-Line Utility for Converting Bitmap Headers</span></span>

<span data-ttu-id="4f543-173">Bitmap.exe est un utilitaire de ligne de commande situé dans le \\ dossier bin sous le dossier d’installation que vous avez spécifié.</span><span class="sxs-lookup"><span data-stu-id="4f543-173">Bitmap.exe is a command-line utility located in the \\Bin folder under the installation folder that you specified.</span></span> <span data-ttu-id="4f543-174">Il modifie les en-têtes des bitmaps Windows, ce qui vous permet de convertir les bitmaps existantes des structures d’en-tête **BITMAPINFOHEADER** et **BITMAPV4HEADER** vers la nouvelle structure **BITMAPV5HEADER** , puis de les replacer.</span><span class="sxs-lookup"><span data-stu-id="4f543-174">It modifies the headers of Windows bitmaps, allowing you to convert existing bitmaps from **BITMAPINFOHEADER** and **BITMAPV4HEADER** header structures to the newer **BITMAPV5HEADER** structure and back again.</span></span> <span data-ttu-id="4f543-175">La syntaxe de la ligne de commande est la suivante :</span><span class="sxs-lookup"><span data-stu-id="4f543-175">The command-line syntax is as follows:</span></span>


```C++
BITMAP [/d] [/1|4|5] [/s] [/f] 
filename
```



<span data-ttu-id="4f543-176">Les commutateurs de ligne de commande ont les effets suivants.</span><span class="sxs-lookup"><span data-stu-id="4f543-176">The command-line switches have the following effects.</span></span>



| <span data-ttu-id="4f543-177">Commutateur</span><span class="sxs-lookup"><span data-stu-id="4f543-177">Switch</span></span> | <span data-ttu-id="4f543-178">Signification</span><span class="sxs-lookup"><span data-stu-id="4f543-178">Meaning</span></span>                                                                  |
|--------|--------------------------------------------------------------------------|
| <span data-ttu-id="4f543-179">/d</span><span class="sxs-lookup"><span data-stu-id="4f543-179">/d</span></span>     | <span data-ttu-id="4f543-180">Les valeurs par défaut sont automatiquement entrées dans les en-têtes convertis.</span><span class="sxs-lookup"><span data-stu-id="4f543-180">Default values are automatically entered in the converted headers.</span></span>       |
| <span data-ttu-id="4f543-181">/1</span><span class="sxs-lookup"><span data-stu-id="4f543-181">/1</span></span>     | <span data-ttu-id="4f543-182">Convertir les bitmaps spécifiées en **BITMAPINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="4f543-182">Convert the specified bitmaps to **BITMAPINFOHEADER**</span></span>                    |
| <span data-ttu-id="4f543-183">/4</span><span class="sxs-lookup"><span data-stu-id="4f543-183">/4</span></span>     | <span data-ttu-id="4f543-184">Convertir les bitmaps spécifiées en **BITMAPV4HEADER**</span><span class="sxs-lookup"><span data-stu-id="4f543-184">Convert the specified bitmaps to **BITMAPV4HEADER**</span></span>                      |
| <span data-ttu-id="4f543-185">/5</span><span class="sxs-lookup"><span data-stu-id="4f543-185">/5</span></span>     | <span data-ttu-id="4f543-186">Convertir les bitmaps spécifiées en **BITMAPV5HEADER**</span><span class="sxs-lookup"><span data-stu-id="4f543-186">Convert the specified bitmaps to **BITMAPV5HEADER**</span></span>                      |
| <span data-ttu-id="4f543-187">/f</span><span class="sxs-lookup"><span data-stu-id="4f543-187">/f</span></span>     | <span data-ttu-id="4f543-188">Force la conversion, même si la bitmap a déjà l’en-tête de droite</span><span class="sxs-lookup"><span data-stu-id="4f543-188">Forces conversion, even if the bitmap already has the right header</span></span>       |
| <span data-ttu-id="4f543-189">/s</span><span class="sxs-lookup"><span data-stu-id="4f543-189">/s</span></span>     | <span data-ttu-id="4f543-190">Convertit les bitmaps dans le dossier spécifié et tous les sous-répertoires qu’il contient</span><span class="sxs-lookup"><span data-stu-id="4f543-190">Converts bitmaps in the specified folder and all subdirectories under it</span></span> |



 

 

 