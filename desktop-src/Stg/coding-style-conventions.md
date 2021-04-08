---
title: Conventions de style de codage
description: Les conventions de style de codage sont utilisées dans cette série d’exemples pour faciliter la clarté et la cohérence.
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28e65e19d69f060a5f85d86976c4bd3694f7611
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734964"
---
# <a name="coding-style-conventions"></a><span data-ttu-id="c3672-103">Conventions de style de codage</span><span class="sxs-lookup"><span data-stu-id="c3672-103">Coding Style Conventions</span></span>

<span data-ttu-id="c3672-104">Les conventions de style de codage sont utilisées dans cette série d’exemples pour faciliter la clarté et la cohérence.</span><span class="sxs-lookup"><span data-stu-id="c3672-104">Coding style conventions are used in this sample series to aid clarity and consistency.</span></span> <span data-ttu-id="c3672-105">Les conventions de notation « hongrois » sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="c3672-105">The "Hungarian" notation conventions are used.</span></span> <span data-ttu-id="c3672-106">Ils sont devenus une pratique de codage courante dans la programmation Win32.</span><span class="sxs-lookup"><span data-stu-id="c3672-106">These have become a common coding practice in Win32 programming.</span></span> <span data-ttu-id="c3672-107">Elles incluent des notations de préfixe variables qui donnent à des noms de variables une suggestion du type de la variable.</span><span class="sxs-lookup"><span data-stu-id="c3672-107">They include variable prefix notations that give to variable names a suggestion of the type of the variable.</span></span>

<span data-ttu-id="c3672-108">Le tableau suivant répertorie les préfixes courants.</span><span class="sxs-lookup"><span data-stu-id="c3672-108">The following table lists common prefixes.</span></span>



| <span data-ttu-id="c3672-109">Préfixe</span><span class="sxs-lookup"><span data-stu-id="c3672-109">Prefix</span></span> | <span data-ttu-id="c3672-110">Description</span><span class="sxs-lookup"><span data-stu-id="c3672-110">Description</span></span>                         |
|--------|-------------------------------------|
| <span data-ttu-id="c3672-111">a</span><span class="sxs-lookup"><span data-stu-id="c3672-111">a</span></span>      | <span data-ttu-id="c3672-112">Array</span><span class="sxs-lookup"><span data-stu-id="c3672-112">Array</span></span>                               |
| <span data-ttu-id="c3672-113">b</span><span class="sxs-lookup"><span data-stu-id="c3672-113">b</span></span>      | <span data-ttu-id="c3672-114">BOOL (int)</span><span class="sxs-lookup"><span data-stu-id="c3672-114">BOOL (int)</span></span>                          |
| <span data-ttu-id="c3672-115">c</span><span class="sxs-lookup"><span data-stu-id="c3672-115">c</span></span>      | <span data-ttu-id="c3672-116">Char</span><span class="sxs-lookup"><span data-stu-id="c3672-116">Char</span></span>                                |
| <span data-ttu-id="c3672-117">libéré</span><span class="sxs-lookup"><span data-stu-id="c3672-117">cb</span></span>     | <span data-ttu-id="c3672-118">Nombre d’octets</span><span class="sxs-lookup"><span data-stu-id="c3672-118">Count of bytes</span></span>                      |
| <span data-ttu-id="c3672-119">cr</span><span class="sxs-lookup"><span data-stu-id="c3672-119">cr</span></span>     | <span data-ttu-id="c3672-120">Valeur de référence de couleur</span><span class="sxs-lookup"><span data-stu-id="c3672-120">Color reference value</span></span>               |
| <span data-ttu-id="c3672-121">adéquat</span><span class="sxs-lookup"><span data-stu-id="c3672-121">cx</span></span>     | <span data-ttu-id="c3672-122">Nombre de x (short)</span><span class="sxs-lookup"><span data-stu-id="c3672-122">Count of x (short)</span></span>                  |
| <span data-ttu-id="c3672-123">dw</span><span class="sxs-lookup"><span data-stu-id="c3672-123">dw</span></span>     | <span data-ttu-id="c3672-124">DWORD (unsigned long)</span><span class="sxs-lookup"><span data-stu-id="c3672-124">DWORD (unsigned long)</span></span>               |
| <span data-ttu-id="c3672-125">f</span><span class="sxs-lookup"><span data-stu-id="c3672-125">f</span></span>      | <span data-ttu-id="c3672-126">Indicateurs (généralement plusieurs valeurs de bits)</span><span class="sxs-lookup"><span data-stu-id="c3672-126">Flags (usually multiple bit values)</span></span> |
| <span data-ttu-id="c3672-127">fn</span><span class="sxs-lookup"><span data-stu-id="c3672-127">fn</span></span>     | <span data-ttu-id="c3672-128">Fonction</span><span class="sxs-lookup"><span data-stu-id="c3672-128">Function</span></span>                            |
| <span data-ttu-id="c3672-129">activée\_</span><span class="sxs-lookup"><span data-stu-id="c3672-129">g\_</span></span>    | <span data-ttu-id="c3672-130">Global</span><span class="sxs-lookup"><span data-stu-id="c3672-130">Global</span></span>                              |
| <span data-ttu-id="c3672-131">h</span><span class="sxs-lookup"><span data-stu-id="c3672-131">h</span></span>      | <span data-ttu-id="c3672-132">Handle</span><span class="sxs-lookup"><span data-stu-id="c3672-132">Handle</span></span>                              |
| <span data-ttu-id="c3672-133">i</span><span class="sxs-lookup"><span data-stu-id="c3672-133">i</span></span>      | <span data-ttu-id="c3672-134">Integer</span><span class="sxs-lookup"><span data-stu-id="c3672-134">Integer</span></span>                             |
| <span data-ttu-id="c3672-135">l</span><span class="sxs-lookup"><span data-stu-id="c3672-135">l</span></span>      | <span data-ttu-id="c3672-136">Long</span><span class="sxs-lookup"><span data-stu-id="c3672-136">Long</span></span>                                |
| <span data-ttu-id="c3672-137">lp</span><span class="sxs-lookup"><span data-stu-id="c3672-137">lp</span></span>     | <span data-ttu-id="c3672-138">Pointeur long</span><span class="sxs-lookup"><span data-stu-id="c3672-138">Long pointer</span></span>                        |
| <span data-ttu-id="c3672-139">lecteur\_</span><span class="sxs-lookup"><span data-stu-id="c3672-139">m\_</span></span>    | <span data-ttu-id="c3672-140">Données membres d’une classe</span><span class="sxs-lookup"><span data-stu-id="c3672-140">Data member of a class</span></span>              |
| <span data-ttu-id="c3672-141">n</span><span class="sxs-lookup"><span data-stu-id="c3672-141">n</span></span>      | <span data-ttu-id="c3672-142">Entier Short</span><span class="sxs-lookup"><span data-stu-id="c3672-142">Short int</span></span>                           |
| <span data-ttu-id="c3672-143">p</span><span class="sxs-lookup"><span data-stu-id="c3672-143">p</span></span>      | <span data-ttu-id="c3672-144">Pointeur</span><span class="sxs-lookup"><span data-stu-id="c3672-144">Pointer</span></span>                             |
| <span data-ttu-id="c3672-145">s</span><span class="sxs-lookup"><span data-stu-id="c3672-145">s</span></span>      | <span data-ttu-id="c3672-146">String</span><span class="sxs-lookup"><span data-stu-id="c3672-146">String</span></span>                              |
| <span data-ttu-id="c3672-147">sz</span><span class="sxs-lookup"><span data-stu-id="c3672-147">sz</span></span>     | <span data-ttu-id="c3672-148">Chaîne terminée par zéro</span><span class="sxs-lookup"><span data-stu-id="c3672-148">Zero terminated String</span></span>              |
| <span data-ttu-id="c3672-149">tm</span><span class="sxs-lookup"><span data-stu-id="c3672-149">tm</span></span>     | <span data-ttu-id="c3672-150">Mesure du texte</span><span class="sxs-lookup"><span data-stu-id="c3672-150">Text metric</span></span>                         |
| <span data-ttu-id="c3672-151">u</span><span class="sxs-lookup"><span data-stu-id="c3672-151">u</span></span>      | <span data-ttu-id="c3672-152">Entier non signé</span><span class="sxs-lookup"><span data-stu-id="c3672-152">Unsigned int</span></span>                        |
| <span data-ttu-id="c3672-153">UL</span><span class="sxs-lookup"><span data-stu-id="c3672-153">ul</span></span>     | <span data-ttu-id="c3672-154">Unsigned long (ULONG)</span><span class="sxs-lookup"><span data-stu-id="c3672-154">Unsigned long (ULONG)</span></span>               |
| <span data-ttu-id="c3672-155">w</span><span class="sxs-lookup"><span data-stu-id="c3672-155">w</span></span>      | <span data-ttu-id="c3672-156">WORD (unsigned short)</span><span class="sxs-lookup"><span data-stu-id="c3672-156">WORD (unsigned short)</span></span>               |
| <span data-ttu-id="c3672-157">x, y</span><span class="sxs-lookup"><span data-stu-id="c3672-157">x,y</span></span>    | <span data-ttu-id="c3672-158">coordonnées x, y (short)</span><span class="sxs-lookup"><span data-stu-id="c3672-158">x, y coordinates (short)</span></span>            |



 

<span data-ttu-id="c3672-159">Elles sont souvent combinées, comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="c3672-159">These are often combined, as in the following.</span></span>



| <span data-ttu-id="c3672-160">Combinaison de préfixes</span><span class="sxs-lookup"><span data-stu-id="c3672-160">Prefix combination</span></span> | <span data-ttu-id="c3672-161">Description</span><span class="sxs-lookup"><span data-stu-id="c3672-161">Description</span></span>                                             |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="c3672-162">pszMyString</span><span class="sxs-lookup"><span data-stu-id="c3672-162">pszMyString</span></span>        | <span data-ttu-id="c3672-163">Pointeur vers une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c3672-163">A pointer to a string.</span></span>                                  |
| <span data-ttu-id="c3672-164">m \_ pszMyString</span><span class="sxs-lookup"><span data-stu-id="c3672-164">m\_pszMyString</span></span>     | <span data-ttu-id="c3672-165">Pointeur vers une chaîne qui est un membre de données d’une classe.</span><span class="sxs-lookup"><span data-stu-id="c3672-165">A pointer to a string that is a data member of a class.</span></span> |



 

<span data-ttu-id="c3672-166">Les autres conventions sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c3672-166">Other conventions are listed in the following table.</span></span>



| <span data-ttu-id="c3672-167">Convention</span><span class="sxs-lookup"><span data-stu-id="c3672-167">Convention</span></span>       | <span data-ttu-id="c3672-168">Description</span><span class="sxs-lookup"><span data-stu-id="c3672-168">Description</span></span>                                              |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="c3672-169">Étiquettes</span><span class="sxs-lookup"><span data-stu-id="c3672-169">CMyClass</span></span>         | <span data-ttu-id="c3672-170">Préfixe’C’pour les noms de classe C++.</span><span class="sxs-lookup"><span data-stu-id="c3672-170">Prefix 'C' for C++ class names.</span></span>                          |
| <span data-ttu-id="c3672-171">COMyObjectClass</span><span class="sxs-lookup"><span data-stu-id="c3672-171">COMyObjectClass</span></span>  | <span data-ttu-id="c3672-172">Préfixe’CO’pour les noms de classes d’objets COM.</span><span class="sxs-lookup"><span data-stu-id="c3672-172">Prefix 'CO' for COM object class names.</span></span>                  |
| <span data-ttu-id="c3672-173">CFMyClassFactory</span><span class="sxs-lookup"><span data-stu-id="c3672-173">CFMyClassFactory</span></span> | <span data-ttu-id="c3672-174">Préfixe « CF » pour les noms de fabrique de classes COM.</span><span class="sxs-lookup"><span data-stu-id="c3672-174">Prefix 'CF' for COM class factory names.</span></span>                 |
| <span data-ttu-id="c3672-175">IMyInterface</span><span class="sxs-lookup"><span data-stu-id="c3672-175">IMyInterface</span></span>     | <span data-ttu-id="c3672-176">Préfixe’I’pour les noms de classe d’interface COM.</span><span class="sxs-lookup"><span data-stu-id="c3672-176">Prefix 'I' for COM interface class names.</span></span>                |
| <span data-ttu-id="c3672-177">CImpIMyInterface</span><span class="sxs-lookup"><span data-stu-id="c3672-177">CImpIMyInterface</span></span> | <span data-ttu-id="c3672-178">Préfixe’CImpI’pour les classes d’implémentation de l’interface COM.</span><span class="sxs-lookup"><span data-stu-id="c3672-178">Prefix 'CImpI' for COM interface implementation classes.</span></span> |



 

<span data-ttu-id="c3672-179">Certaines conventions cohérentes pour les blocs d’en-tête de commentaire sont utilisées dans cette série d’exemples comme suit.</span><span class="sxs-lookup"><span data-stu-id="c3672-179">Some consistent conventions for comment header blocks are used in this sample series as follows.</span></span>

## <a name="file-header"></a><span data-ttu-id="c3672-180">En-tête de fichier</span><span class="sxs-lookup"><span data-stu-id="c3672-180">File Header</span></span>

``` syntax
/*+===================================================================
  File:      MYFILE.EXT

  Summary:   Brief summary of the file contents and purpose.

  Classes:   Classes declared or used (in source files).

  Functions: Functions exported (in source files).

  Origin:    Indications of where content may have come from. This
             is not a change history but rather a reference to the
             editor-inheritance behind the content or other
             indications about the origin of the source.

  Copyright and Legal notices.
  Copyright and Legal notices.
===================================================================+*/
```

## <a name="plain-comment-block"></a><span data-ttu-id="c3672-181">Bloc de commentaire brut</span><span class="sxs-lookup"><span data-stu-id="c3672-181">Plain Comment Block</span></span>

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a><span data-ttu-id="c3672-182">En-tête de déclaration de classe</span><span class="sxs-lookup"><span data-stu-id="c3672-182">Class Declaration Header</span></span>

``` syntax
/*C+C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C
  Class:    CMyClass

  Summary:  Short summary of purpose and content of CMyClass.
            Short summary of purpose and content of CMyClass.

  Methods:  MyMethodOne
              Short description of MyMethodOne.
            MyMethodTwo
              Short description of MyMethodTwo.
            CMyClass
              Constructor.
            ~CMyClass
              Destructor.
C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C-C*/
```

## <a name="class-method-definition-header"></a><span data-ttu-id="c3672-183">En-tête de définition de méthode de classe</span><span class="sxs-lookup"><span data-stu-id="c3672-183">Class Method Definition Header</span></span>

``` syntax
/*M+M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M
  Method:   CMyClass::MyMethodOne

  Summary:  Short summary of purpose and content of MyMethodOne.
            Short summary of purpose and content of MyMethodOne.

  Args:     MYTYPE MyArgOne
              Short description of argument MyArgOne.
            MYTYPE MyArgTwo
              Short description of argument MyArgTwo.

  Modifies: [list of member data variables modified by this method].

  Returns:  MYRETURNTYPE
              Short description of meaning of the return type values.
M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M-M*/
```

## <a name="unexported-or-local-function"></a><span data-ttu-id="c3672-184">Fonction non exportée ou locale</span><span class="sxs-lookup"><span data-stu-id="c3672-184">Unexported or Local Function</span></span>

``` syntax
/*F+F+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
  Function: MyLocalFunction

  Summary:  What MyLocalFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
-----------------------------------------------------------------F-F*/
```

## <a name="exported-function-definition-header"></a><span data-ttu-id="c3672-185">En-tête de définition de fonction exportée</span><span class="sxs-lookup"><span data-stu-id="c3672-185">Exported Function Definition Header</span></span>

``` syntax
/*F+F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F
  Function: MyFunction

  Summary:  What MyFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F-F*/
```

## <a name="com-interface-declaration-header"></a><span data-ttu-id="c3672-186">En-tête de déclaration de l’interface COM</span><span class="sxs-lookup"><span data-stu-id="c3672-186">COM Interface Declaration Header</span></span>

``` syntax
/*I+I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I
  Interface: IMyInterface

  Summary:   Short summary of what features the interface can bring to
             a COM Component.

  Methods:   MYTYPE MyMethodOne
               Description.
             MYTYPE MyMethodTwo
               Description.
I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I-I*/
```

## <a name="com-object-class-declaration-header"></a><span data-ttu-id="c3672-187">En-tête de déclaration de classe d’objets COM</span><span class="sxs-lookup"><span data-stu-id="c3672-187">COM Object Class Declaration Header</span></span>

``` syntax
/*O+O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O
  ObjectClass: COMyCOMObject

  Summary:     Short summary of purpose and content of this object.

  Interfaces:  IUnknown
                 Standard interface providing COM object features.
               IMyInterfaceOne
                 Description.
               IMyInterfaceTwo
                 Description.

  Aggregation: [whether this COM Object is aggregatable or not]
O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O-O*/
```

<span data-ttu-id="c3672-188">Toutes ces conventions de bloc de commentaires ont des chaînes de jeton de début et de fin cohérentes.</span><span class="sxs-lookup"><span data-stu-id="c3672-188">All of these comment block conventions have consistent beginning and ending token strings.</span></span> <span data-ttu-id="c3672-189">Cette cohérence prend en charge le traitement automatique des en-têtes d’une certaine manière.</span><span class="sxs-lookup"><span data-stu-id="c3672-189">This consistency supports automatic processing of the headers in some fashion.</span></span> <span data-ttu-id="c3672-190">Par exemple, les scripts AWK peuvent être écrits pour filtrer les en-têtes de fonction dans un fichier texte distinct qui peut ensuite servir de base pour un document de spécification.</span><span class="sxs-lookup"><span data-stu-id="c3672-190">For example, AWK scripts can be written to filter the function headers into a separate text file that can then serve as the basis for a specification document.</span></span> <span data-ttu-id="c3672-191">De même, les outils tels que l’utilitaire autoduck non pris en charge (actuellement disponible sur le CD-ROM de la bibliothèque de développement Microsoft Developer Network) peuvent être utilisés pour traiter les blocs de commentaires dans ces en-têtes.</span><span class="sxs-lookup"><span data-stu-id="c3672-191">Similarly, tools like the unsupported AUTODUCK utility (currently available on the Microsoft Developer Network Development Library CD-ROM) can be used to process the comment blocks in these headers.</span></span>

<span data-ttu-id="c3672-192">Le tableau suivant répertorie les chaînes de jetons de début et de fin utilisées dans les exemples de didacticiels.</span><span class="sxs-lookup"><span data-stu-id="c3672-192">The following table lists beginning and ending token strings used in sample tutorials.</span></span>



| <span data-ttu-id="c3672-193">par jeton</span><span class="sxs-lookup"><span data-stu-id="c3672-193">Token</span></span> | <span data-ttu-id="c3672-194">Description</span><span class="sxs-lookup"><span data-stu-id="c3672-194">Description</span></span>                      |
|-------|----------------------------------|
| /\*+  | <span data-ttu-id="c3672-195">Début de l’en-tête de fichier</span><span class="sxs-lookup"><span data-stu-id="c3672-195">File Header Begin</span></span>                |
| +\*/  | <span data-ttu-id="c3672-196">Fin d’en-tête de fichier</span><span class="sxs-lookup"><span data-stu-id="c3672-196">File Header End</span></span>                  |
| /\*-  | <span data-ttu-id="c3672-197">Début de l’en-tête de bloc de commentaire brut</span><span class="sxs-lookup"><span data-stu-id="c3672-197">Plain comment block Header Begin</span></span> |
| -\*/  | <span data-ttu-id="c3672-198">Fin d’en-tête de bloc de commentaire brut</span><span class="sxs-lookup"><span data-stu-id="c3672-198">Plain comment block Header End</span></span>   |
| <span data-ttu-id="c3672-199">/\*Secteur</span><span class="sxs-lookup"><span data-stu-id="c3672-199">/\*C</span></span>  | <span data-ttu-id="c3672-200">Début de l’en-tête de classe</span><span class="sxs-lookup"><span data-stu-id="c3672-200">Class Header Begin</span></span>               |
| <span data-ttu-id="c3672-201">Secteur\*/</span><span class="sxs-lookup"><span data-stu-id="c3672-201">C\*/</span></span>  | <span data-ttu-id="c3672-202">Fin d’en-tête de classe</span><span class="sxs-lookup"><span data-stu-id="c3672-202">Class Header End</span></span>                 |
| <span data-ttu-id="c3672-203">/\*Lecteur</span><span class="sxs-lookup"><span data-stu-id="c3672-203">/\*M</span></span>  | <span data-ttu-id="c3672-204">Début de l’en-tête de méthode</span><span class="sxs-lookup"><span data-stu-id="c3672-204">Method Header Begin</span></span>              |
| <span data-ttu-id="c3672-205">Lecteur\*/</span><span class="sxs-lookup"><span data-stu-id="c3672-205">M\*/</span></span>  | <span data-ttu-id="c3672-206">Fin de l’en-tête de méthode</span><span class="sxs-lookup"><span data-stu-id="c3672-206">Method Header End</span></span>                |
| <span data-ttu-id="c3672-207">/\*FA</span><span class="sxs-lookup"><span data-stu-id="c3672-207">/\*F</span></span>  | <span data-ttu-id="c3672-208">Début de l’en-tête de fonction</span><span class="sxs-lookup"><span data-stu-id="c3672-208">Function Header Begin</span></span>            |
| <span data-ttu-id="c3672-209">FA\*/</span><span class="sxs-lookup"><span data-stu-id="c3672-209">F\*/</span></span>  | <span data-ttu-id="c3672-210">Fin d’en-tête de fonction</span><span class="sxs-lookup"><span data-stu-id="c3672-210">Function Header End</span></span>              |
| <span data-ttu-id="c3672-211">/\*Cliqu</span><span class="sxs-lookup"><span data-stu-id="c3672-211">/\*I</span></span>  | <span data-ttu-id="c3672-212">Début de l’en-tête d’interface</span><span class="sxs-lookup"><span data-stu-id="c3672-212">Interface Header Begin</span></span>           |
| <span data-ttu-id="c3672-213">Cliqu\*/</span><span class="sxs-lookup"><span data-stu-id="c3672-213">I\*/</span></span>  | <span data-ttu-id="c3672-214">Fin d’en-tête d’interface</span><span class="sxs-lookup"><span data-stu-id="c3672-214">Interface Header End</span></span>             |
| <span data-ttu-id="c3672-215">/\*Sorties</span><span class="sxs-lookup"><span data-stu-id="c3672-215">/\*O</span></span>  | <span data-ttu-id="c3672-216">Début de l’en-tête de classe d’objet COM</span><span class="sxs-lookup"><span data-stu-id="c3672-216">COM Object Class Header Begin</span></span>    |
| <span data-ttu-id="c3672-217">Sorties\*/</span><span class="sxs-lookup"><span data-stu-id="c3672-217">O\*/</span></span>  | <span data-ttu-id="c3672-218">Fin d’en-tête de classe d’objet COM</span><span class="sxs-lookup"><span data-stu-id="c3672-218">COM Object Class Header End</span></span>      |



 

<span data-ttu-id="c3672-219">Ces en-têtes peuvent également être utilisés comme signaux visuels pour une analyse rapide des fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="c3672-219">These headers can also be used as visual cues for rapid scanning of source files.</span></span> <span data-ttu-id="c3672-220">Ils facilitent également l’obtention rapide d’un emplacement source si vous configurez des chaînes de recherche dans votre éditeur, puis « répéter la dernière recherche » pour localiser rapidement ces en-têtes.</span><span class="sxs-lookup"><span data-stu-id="c3672-220">They also provide convenience for rapidly getting to some source location if you set up search strings in your editor and then 'repeat last search' to quickly locate these headers.</span></span>

<span data-ttu-id="c3672-221">Par exemple, la chaîne de recherche « M + M » localise le début des en-têtes de la méthode et « M-M » localise le début du code réel de la définition de la méthode/de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="c3672-221">For example, the search string "M+M" will locate the start of method headers, and "M-M" will locate the beginning of the actual method definition/implementation code.</span></span>

 

 




