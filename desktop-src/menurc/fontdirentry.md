---
title: FONTDIRENTRY, structure
description: Contient des informations sur une police individuelle dans un groupe de ressources de polices. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- Menus de la structure FONTDIRENTRY et autres ressources
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1cee72a490fd2b94b1c810797f656d81418c0f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464678"
---
# <a name="fontdirentry-structure"></a><span data-ttu-id="6da80-105">FONTDIRENTRY, structure</span><span class="sxs-lookup"><span data-stu-id="6da80-105">FONTDIRENTRY structure</span></span>

<span data-ttu-id="6da80-106">Contient des informations sur une police individuelle dans un groupe de ressources de polices.</span><span class="sxs-lookup"><span data-stu-id="6da80-106">Contains information about an individual font in a font resource group.</span></span> <span data-ttu-id="6da80-107">La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="6da80-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6da80-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6da80-108">Syntax</span></span>


```C++
typedef struct {
  WORD  dfVersion;
  DWORD dfSize;
  CHAR  dfCopyright[60];
  WORD  dfType;
  WORD  dfPoints;
  WORD  dfVertRes;
  WORD  dfHorizRes;
  WORD  dfAscent;
  WORD  dfInternalLeading;
  WORD  dfExternalLeading;
  BYTE  dfItalic;
  BYTE  dfUnderline;
  BYTE  dfStrikeOut;
  WORD  dfWeight;
  BYTE  dfCharSet;
  WORD  dfPixWidth;
  WORD  dfPixHeight;
  BYTE  dfPitchAndFamily;
  WORD  dfAvgWidth;
  WORD  dfMaxWidth;
  BYTE  dfFirstChar;
  BYTE  dfLastChar;
  BYTE  dfDefaultChar;
  BYTE  dfBreakChar;
  WORD  dfWidthBytes;
  DWORD dfDevice;
  DWORD dfFace;
  DWORD dfReserved;
  CHAR  szDeviceName;
  CHAR  szFaceName;
} FONTDIRENTRY;
```



## <a name="members"></a><span data-ttu-id="6da80-109">Membres</span><span class="sxs-lookup"><span data-stu-id="6da80-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="6da80-110">**dfVersion**</span><span class="sxs-lookup"><span data-stu-id="6da80-110">**dfVersion**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="6da80-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-112">Numéro de version défini par l’utilisateur pour les données de ressources que les outils peuvent utiliser pour lire et écrire des fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="6da80-112">A user-defined version number for the resource data that tools can use to read and write resource files.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-113">**dfSize**</span><span class="sxs-lookup"><span data-stu-id="6da80-113">**dfSize**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-114">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6da80-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-115">Taille du fichier, en octets.</span><span class="sxs-lookup"><span data-stu-id="6da80-115">The size of the file, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-116">**dfCopyright \[ 60\]**</span><span class="sxs-lookup"><span data-stu-id="6da80-116">**dfCopyright\[60\]**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-117">Type : **char**</span><span class="sxs-lookup"><span data-stu-id="6da80-117">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-118">Informations de copyright du fournisseur de polices.</span><span class="sxs-lookup"><span data-stu-id="6da80-118">The font supplier's copyright information.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-119">**dfType**</span><span class="sxs-lookup"><span data-stu-id="6da80-119">**dfType**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-120">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="6da80-120">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-121">Type de fichier de polices.</span><span class="sxs-lookup"><span data-stu-id="6da80-121">The type of font file.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-122">**dfPoints**</span><span class="sxs-lookup"><span data-stu-id="6da80-122">**dfPoints**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-123">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="6da80-123">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-124">Taille en points à laquelle ce jeu de caractères ressemble le mieux.</span><span class="sxs-lookup"><span data-stu-id="6da80-124">The point size at which this character set looks best.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-125">**dfVertRes**</span><span class="sxs-lookup"><span data-stu-id="6da80-125">**dfVertRes**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-126">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="6da80-126">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-127">Résolution verticale, en points par pouce, à laquelle ce jeu de caractères a été numérisé.</span><span class="sxs-lookup"><span data-stu-id="6da80-127">The vertical resolution, in dots per inch, at which this character set was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-128">**dfHorizRes**</span><span class="sxs-lookup"><span data-stu-id="6da80-128">**dfHorizRes**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-129">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="6da80-129">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-130">Résolution horizontale, en points par pouce, à laquelle ce jeu de caractères a été numérisé.</span><span class="sxs-lookup"><span data-stu-id="6da80-130">The horizontal resolution, in dots per inch, at which this character set was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-131">**dfAscent**</span><span class="sxs-lookup"><span data-stu-id="6da80-131">**dfAscent**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-132">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="6da80-132">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-133">Distance entre le haut d’une cellule de définition de caractère et la ligne de base de la police typographique.</span><span class="sxs-lookup"><span data-stu-id="6da80-133">The distance from the top of a character definition cell to the baseline of the typographical font.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-134">**dfInternalLeading**</span><span class="sxs-lookup"><span data-stu-id="6da80-134">**dfInternalLeading**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-135">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="6da80-135">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-136">Quantité de début dans les limites définies par le membre **dfPixHeight** .</span><span class="sxs-lookup"><span data-stu-id="6da80-136">The amount of leading inside the bounds set by the **dfPixHeight** member.</span></span> <span data-ttu-id="6da80-137">Des marques d’accentuation et d’autres caractères diacritiques peuvent se produire dans cette zone.</span><span class="sxs-lookup"><span data-stu-id="6da80-137">Accent marks and other diacritical characters can occur in this area.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-138">**dfExternalLeading**</span><span class="sxs-lookup"><span data-stu-id="6da80-138">**dfExternalLeading**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-139">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="6da80-139">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-140">Quantité d’espace de tête supplémentaire que l’application ajoute entre les lignes.</span><span class="sxs-lookup"><span data-stu-id="6da80-140">The amount of extra leading that the application adds between rows.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-141">**dfItalic**</span><span class="sxs-lookup"><span data-stu-id="6da80-141">**dfItalic**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-142">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="6da80-142">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-143">Police en italique s’il n’est pas égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="6da80-143">An italic font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-144">**dfUnderline**</span><span class="sxs-lookup"><span data-stu-id="6da80-144">**dfUnderline**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-145">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="6da80-145">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-146">Police soulignée s’il n’est pas égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="6da80-146">An underlined font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-147">**dfStrikeOut**</span><span class="sxs-lookup"><span data-stu-id="6da80-147">**dfStrikeOut**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-148">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="6da80-148">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-149">Police de barré s’il n’est pas égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="6da80-149">A strikeout font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-150">**dfWeight**</span><span class="sxs-lookup"><span data-stu-id="6da80-150">**dfWeight**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-151">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="6da80-151">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-152">Poids de la police dans la plage comprise entre 0 et 1000.</span><span class="sxs-lookup"><span data-stu-id="6da80-152">The weight of the font in the range 0 through 1000.</span></span> <span data-ttu-id="6da80-153">Par exemple, 400 est roman et 700 est gras.</span><span class="sxs-lookup"><span data-stu-id="6da80-153">For example, 400 is roman and 700 is bold.</span></span> <span data-ttu-id="6da80-154">Si cette valeur est égale à zéro, une pondération par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="6da80-154">If this value is zero, a default weight is used.</span></span> <span data-ttu-id="6da80-155">Pour obtenir des valeurs définies supplémentaires, consultez la description de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="6da80-155">For additional defined values, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-156">**dfCharSet**</span><span class="sxs-lookup"><span data-stu-id="6da80-156">**dfCharSet**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-157">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="6da80-157">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-158">Jeu de caractères de la police.</span><span class="sxs-lookup"><span data-stu-id="6da80-158">The character set of the font.</span></span> <span data-ttu-id="6da80-159">Pour les valeurs prédéfinies, consultez la description de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="6da80-159">For predefined values, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-160">**dfPixWidth**</span><span class="sxs-lookup"><span data-stu-id="6da80-160">**dfPixWidth**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-161">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="6da80-161">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-162">Largeur de la grille sur laquelle une police vectorielle a été numérisée.</span><span class="sxs-lookup"><span data-stu-id="6da80-162">The width of the grid on which a vector font was digitized.</span></span> <span data-ttu-id="6da80-163">Pour les polices Raster, si le membre n’est pas égal à zéro, il représente la largeur de tous les caractères de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="6da80-163">For raster fonts, if the member is not equal to zero, it represents the width for all the characters in the bitmap.</span></span> <span data-ttu-id="6da80-164">Si le membre est égal à zéro, la police a des caractères de largeur variable.</span><span class="sxs-lookup"><span data-stu-id="6da80-164">If the member is equal to zero, the font has variable-width characters.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-165">**dfPixHeight**</span><span class="sxs-lookup"><span data-stu-id="6da80-165">**dfPixHeight**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-166">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="6da80-166">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-167">Hauteur de la bitmap de caractères pour les polices Raster ou la hauteur de la grille sur laquelle une police vectorielle a été numérisée.</span><span class="sxs-lookup"><span data-stu-id="6da80-167">The height of the character bitmap for raster fonts or the height of the grid on which a vector font was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-168">**dfPitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="6da80-168">**dfPitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-169">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="6da80-169">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-170">Le pas et la famille de la police.</span><span class="sxs-lookup"><span data-stu-id="6da80-170">The pitch and the family of the font.</span></span> <span data-ttu-id="6da80-171">Pour plus d’informations, consultez la description de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="6da80-171">For additional information, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-172">**dfAvgWidth**</span><span class="sxs-lookup"><span data-stu-id="6da80-172">**dfAvgWidth**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-173">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="6da80-173">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-174">Largeur moyenne des caractères de la police (généralement définie en tant que largeur de la lettre x).</span><span class="sxs-lookup"><span data-stu-id="6da80-174">The average width of characters in the font (generally defined as the width of the letter x).</span></span> <span data-ttu-id="6da80-175">Cette valeur n’inclut pas le dépassement requis pour les caractères gras ou italiques.</span><span class="sxs-lookup"><span data-stu-id="6da80-175">This value does not include the overhang required for bold or italic characters.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-176">**dfMaxWidth**</span><span class="sxs-lookup"><span data-stu-id="6da80-176">**dfMaxWidth**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-177">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="6da80-177">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-178">La largeur du caractère le plus large de la police.</span><span class="sxs-lookup"><span data-stu-id="6da80-178">The width of the widest character in the font.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-179">**dfFirstChar**</span><span class="sxs-lookup"><span data-stu-id="6da80-179">**dfFirstChar**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-180">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="6da80-180">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-181">Premier code de caractère défini dans la police.</span><span class="sxs-lookup"><span data-stu-id="6da80-181">The first character code defined in the font.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-182">**dfLastChar**</span><span class="sxs-lookup"><span data-stu-id="6da80-182">**dfLastChar**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-183">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="6da80-183">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-184">Dernier code de caractère défini dans la police.</span><span class="sxs-lookup"><span data-stu-id="6da80-184">The last character code defined in the font.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-185">**dfDefaultChar**</span><span class="sxs-lookup"><span data-stu-id="6da80-185">**dfDefaultChar**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-186">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="6da80-186">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-187">Caractère à substituer aux caractères ne figurant pas dans la police.</span><span class="sxs-lookup"><span data-stu-id="6da80-187">The character to substitute for characters not in the font.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-188">**dfBreakChar**</span><span class="sxs-lookup"><span data-stu-id="6da80-188">**dfBreakChar**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-189">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="6da80-189">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-190">Caractère qui sera utilisé pour définir des césures de mots pour la justification du texte.</span><span class="sxs-lookup"><span data-stu-id="6da80-190">The character that will be used to define word breaks for text justification.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-191">**dfWidthBytes**</span><span class="sxs-lookup"><span data-stu-id="6da80-191">**dfWidthBytes**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-192">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="6da80-192">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-193">Nombre d’octets dans chaque ligne de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="6da80-193">The number of bytes in each row of the bitmap.</span></span> <span data-ttu-id="6da80-194">Cette valeur est toujours même afin que les lignes commencent sur les limites de mot.</span><span class="sxs-lookup"><span data-stu-id="6da80-194">This value is always even so that the rows start on word boundaries.</span></span> <span data-ttu-id="6da80-195">Pour les polices vectorielles, ce membre n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="6da80-195">For vector fonts, this member has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-196">**dfDevice**</span><span class="sxs-lookup"><span data-stu-id="6da80-196">**dfDevice**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-197">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6da80-197">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-198">Offset dans le fichier à une chaîne se terminant par un caractère null qui spécifie un nom de périphérique.</span><span class="sxs-lookup"><span data-stu-id="6da80-198">The offset in the file to a null-terminated string that specifies a device name.</span></span> <span data-ttu-id="6da80-199">Pour une police générique, cette valeur est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="6da80-199">For a generic font, this value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-200">**dfFace**</span><span class="sxs-lookup"><span data-stu-id="6da80-200">**dfFace**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-201">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6da80-201">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-202">Offset dans le fichier à une chaîne se terminant par un caractère null qui nomme le type de caractères.</span><span class="sxs-lookup"><span data-stu-id="6da80-202">The offset in the file to a null-terminated string that names the typeface.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-203">**dfReserved**</span><span class="sxs-lookup"><span data-stu-id="6da80-203">**dfReserved**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-204">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6da80-204">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-205">Ce membre est réservé.</span><span class="sxs-lookup"><span data-stu-id="6da80-205">This member is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-206">**szDeviceName**</span><span class="sxs-lookup"><span data-stu-id="6da80-206">**szDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-207">Type : **char**</span><span class="sxs-lookup"><span data-stu-id="6da80-207">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-208">Nom de l’appareil si ce fichier de police est désigné pour un périphérique spécifique.</span><span class="sxs-lookup"><span data-stu-id="6da80-208">The name of the device if this font file is designated for a specific device.</span></span>

</dd> <dt>

<span data-ttu-id="6da80-209">**szFaceName**</span><span class="sxs-lookup"><span data-stu-id="6da80-209">**szFaceName**</span></span>
</dt> <dd>

<span data-ttu-id="6da80-210">Type : **char**</span><span class="sxs-lookup"><span data-stu-id="6da80-210">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="6da80-211">Nom de police de la police.</span><span class="sxs-lookup"><span data-stu-id="6da80-211">The typeface name of the font.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6da80-212">Notes</span><span class="sxs-lookup"><span data-stu-id="6da80-212">Remarks</span></span>

<span data-ttu-id="6da80-213">Il existe une structure **FONTDIRENTRY** pour chaque police du fichier. res.</span><span class="sxs-lookup"><span data-stu-id="6da80-213">There is one **FONTDIRENTRY** structure for every font in the .res file.</span></span> <span data-ttu-id="6da80-214">Les applications qui génèrent des fichiers. res avec des ressources de police doivent également ajouter au fichier une structure **FONTDIRENTRY** pour chaque police.</span><span class="sxs-lookup"><span data-stu-id="6da80-214">Applications that generate .res files with font resources must also add to the file a **FONTDIRENTRY** structure for each font.</span></span>

<span data-ttu-id="6da80-215">Les déclarations de police peuvent être mélangées à d’autres déclarations de ressource dans le. Fichier RC, car les polices n’ont pas besoin d’être contiguës dans le fichier. res.</span><span class="sxs-lookup"><span data-stu-id="6da80-215">Font declarations can be mixed with other resource declarations in the .RC file because fonts do not need to be contiguous in the .res file.</span></span>

## <a name="requirements"></a><span data-ttu-id="6da80-216">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6da80-216">Requirements</span></span>



| <span data-ttu-id="6da80-217">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6da80-217">Requirement</span></span> | <span data-ttu-id="6da80-218">Valeur</span><span class="sxs-lookup"><span data-stu-id="6da80-218">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6da80-219">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6da80-219">Minimum supported client</span></span><br/> | <span data-ttu-id="6da80-220">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6da80-220">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6da80-221">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6da80-221">Minimum supported server</span></span><br/> | <span data-ttu-id="6da80-222">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6da80-222">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6da80-223">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6da80-223">See also</span></span>

<dl> <dt>

<span data-ttu-id="6da80-224">**Référence**</span><span class="sxs-lookup"><span data-stu-id="6da80-224">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6da80-225">**Dilocataire**</span><span class="sxs-lookup"><span data-stu-id="6da80-225">**DIRENTRY**</span></span>](direntry.md)
</dt> <dt>

[<span data-ttu-id="6da80-226">**FONTGROUPHDR**</span><span class="sxs-lookup"><span data-stu-id="6da80-226">**FONTGROUPHDR**</span></span>](fontgrouphdr.md)
</dt> <dt>

<span data-ttu-id="6da80-227">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="6da80-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6da80-228">Ressources</span><span class="sxs-lookup"><span data-stu-id="6da80-228">Resources</span></span>](resources.md)
</dt> <dt>

<span data-ttu-id="6da80-229">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="6da80-229">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="6da80-230">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="6da80-230">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

