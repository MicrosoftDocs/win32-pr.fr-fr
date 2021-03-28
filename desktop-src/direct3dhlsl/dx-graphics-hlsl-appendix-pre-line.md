---
title: " Line (directive)"
description: Directive de préprocesseur qui définit le numéro de ligne et le nom de fichier stockés en interne du compilateur sur les valeurs spécifiées.
ms.assetid: 307410af-bd78-4b3d-b515-adf58298f35f
keywords:
- Directive de ligne HLSL
topic_type:
- apiref
api_name:
- line Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0932138ce5aec85ad3d3e7058db0c2a93e131181
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380784"
---
# <a name="line-directive"></a><span data-ttu-id="5d994-104">\#Line (directive)</span><span class="sxs-lookup"><span data-stu-id="5d994-104">\#line Directive</span></span>

<span data-ttu-id="5d994-105">Directive de préprocesseur qui définit le numéro de ligne et le nom de fichier stockés en interne du compilateur sur les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="5d994-105">Preprocessor directive that sets the compiler's internally-stored line number and filename to the specified values.</span></span>



| <span data-ttu-id="5d994-106">\#ligne *LineNumber* "*nom_fichier*"</span><span class="sxs-lookup"><span data-stu-id="5d994-106">\#line *lineNumber* "*filename*"</span></span> |
|----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="5d994-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d994-107">Parameters</span></span>



| <span data-ttu-id="5d994-108">Élément</span><span class="sxs-lookup"><span data-stu-id="5d994-108">Item</span></span>                                                                                                                              | <span data-ttu-id="5d994-109">Description</span><span class="sxs-lookup"><span data-stu-id="5d994-109">Description</span></span>                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d994-110"><span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*</span><span class="sxs-lookup"><span data-stu-id="5d994-110"><span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*</span></span><br/>                    | <span data-ttu-id="5d994-111">Numéro de ligne à définir.</span><span class="sxs-lookup"><span data-stu-id="5d994-111">Line number to set.</span></span> <span data-ttu-id="5d994-112">Il peut s’agir de n’importe quelle constante entière.</span><span class="sxs-lookup"><span data-stu-id="5d994-112">This can be any integer constant.</span></span> <span data-ttu-id="5d994-113">Le remplacement des macros peut être effectué sur les jetons de prétraitement, à condition que le résultat corresponde à la syntaxe correcte.</span><span class="sxs-lookup"><span data-stu-id="5d994-113">Macro replacement can be performed on the preprocessing tokens, as long as the result evaluates to the correct syntax.</span></span> <br/>                     |
| <span data-ttu-id="5d994-114"><span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*nom du fichier* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5d994-114"><span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*filename* \[optional\]</span></span> <br/> | <span data-ttu-id="5d994-115">Nom de fichier à définir.</span><span class="sxs-lookup"><span data-stu-id="5d994-115">Filename to set.</span></span> <span data-ttu-id="5d994-116">Le nom de fichier peut être n’importe quelle combinaison de caractères et doit être placé entre guillemets doubles ("").</span><span class="sxs-lookup"><span data-stu-id="5d994-116">The filename can be any combination of characters, and must be enclosed in double quotation marks (" ").</span></span> <span data-ttu-id="5d994-117">Si ce paramètre est omis, le nom de fichier précédent reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="5d994-117">If this parameter is omitted, the previous filename remains unchanged.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="5d994-118">Notes</span><span class="sxs-lookup"><span data-stu-id="5d994-118">Remarks</span></span>

<span data-ttu-id="5d994-119">Le compilateur utilise le numéro de ligne et le nom de fichier pour faire référence aux erreurs qu’il trouve pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="5d994-119">The compiler uses the line number and filename to refer to errors that it finds during compilation.</span></span> <span data-ttu-id="5d994-120">Le numéro de ligne fait généralement référence à la ligne d’entrée en cours et le nom de fichier fait référence au fichier d’entrée en cours.</span><span class="sxs-lookup"><span data-stu-id="5d994-120">The line number usually refers to the current input line, and the filename refers to the current input file.</span></span> <span data-ttu-id="5d994-121">Le numéro de ligne est incrémenté après le traitement de chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="5d994-121">The line number is incremented after each line is processed.</span></span> <span data-ttu-id="5d994-122">Si vous modifiez le numéro de ligne et le nom de fichier, le compilateur ignore les valeurs précédentes et continue le traitement avec les nouvelles valeurs.</span><span class="sxs-lookup"><span data-stu-id="5d994-122">If you change the line number and filename, the compiler ignores the previous values and continues processing with the new values.</span></span> <span data-ttu-id="5d994-123">La \# directive line est généralement utilisée par les générateurs de programmes pour que les messages d’erreur fassent référence au fichier source d’origine et non au programme généré.</span><span class="sxs-lookup"><span data-stu-id="5d994-123">The \#line directive is typically used by program generators to cause error messages to refer to the original source file instead of to the generated program.</span></span>

<span data-ttu-id="5d994-124">Le traducteur utilise le numéro de ligne et le nom de fichier pour déterminer les valeurs du fichier de macros prédéfinies et de la \_ \_ \_ \_ \_ \_ ligne \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5d994-124">The translator uses the line number and filename to determine the values of the predefined macros \_\_FILE\_\_ and \_\_LINE\_\_.</span></span> <span data-ttu-id="5d994-125">Vous pouvez utiliser ces macros pour insérer des messages d’erreur auto-descriptifs dans le texte du programme.</span><span class="sxs-lookup"><span data-stu-id="5d994-125">You can use these macros to insert self-descriptive error messages into the program text.</span></span> <span data-ttu-id="5d994-126">La \_ \_ \_ \_ macro de fichier se développe en une chaîne dont le contenu est le nom de fichier, entouré par des guillemets doubles ("").</span><span class="sxs-lookup"><span data-stu-id="5d994-126">The \_\_FILE\_\_ macro expands to a string whose contents are the filename, surrounded by double quotation marks (" ").</span></span>

## <a name="examples"></a><span data-ttu-id="5d994-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="5d994-127">Examples</span></span>

<span data-ttu-id="5d994-128">L’exemple suivant définit le numéro de ligne sur 151 et le nom de fichier sur « Copy. c ».</span><span class="sxs-lookup"><span data-stu-id="5d994-128">The following example sets the line number to 151 and the filename to "copy.c".</span></span>


```
#line 151 "copy.c"
```



<span data-ttu-id="5d994-129">Dans l’exemple suivant, la macro Assert utilise la ligne et le fichier des macros prédéfinies \_ \_ \_ \_ \_ \_ \_ \_ pour imprimer un message d’erreur relatif au fichier source si l’assertion spécifiée n’a pas la valeur true.</span><span class="sxs-lookup"><span data-stu-id="5d994-129">In the following example, the macro ASSERT uses the predefined macros \_\_LINE\_\_ and \_\_FILE\_\_ to print an error message about the source file if the specified assertion is not true.</span></span>


```
#define ASSERT(cond)

if( !(cond) )\
{printf( "assertion error line %d, file(%s)\n", \
__LINE__, __FILE__ );}
```



## <a name="see-also"></a><span data-ttu-id="5d994-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d994-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d994-131">Directives de préprocesseur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5d994-131">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





