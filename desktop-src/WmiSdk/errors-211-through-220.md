---
description: Décrit les erreurs du fournisseur SNMP WMI 211 à 220.
ms.assetid: beaa644d-51b3-4a57-8853-0b37f69f615a
ms.tgt_platform: multiple
title: Erreurs 211 à 220
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f25dbf8cb8f27d4c58a1505176eca218b8d947d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759435"
---
# <a name="errors-211-through-220"></a><span data-ttu-id="5466c-103">Erreurs 211 à 220</span><span class="sxs-lookup"><span data-stu-id="5466c-103">Errors 211 through 220</span></span>

<span data-ttu-id="5466c-104">Décrit les erreurs du fournisseur SNMP WMI 211 à 220.</span><span class="sxs-lookup"><span data-stu-id="5466c-104">Describes WMI SNMP provider errors 211 through 220.</span></span>

[<span data-ttu-id="5466c-105">Message d’information 211</span><span class="sxs-lookup"><span data-stu-id="5466c-105">Information Message 211</span></span>](#information-message-211)

[<span data-ttu-id="5466c-106">Erreur irrécupérable 212</span><span class="sxs-lookup"><span data-stu-id="5466c-106">Fatal Error 212</span></span>](#fatal-error-212)

[<span data-ttu-id="5466c-107">Erreur irrécupérable 213</span><span class="sxs-lookup"><span data-stu-id="5466c-107">Fatal Error 213</span></span>](#fatal-error-213)

[<span data-ttu-id="5466c-108">Erreur irrécupérable 214</span><span class="sxs-lookup"><span data-stu-id="5466c-108">Fatal Error 214</span></span>](#fatal-error-214)

[<span data-ttu-id="5466c-109">Erreur irrécupérable 215</span><span class="sxs-lookup"><span data-stu-id="5466c-109">Fatal Error 215</span></span>](#fatal-error-215)

[<span data-ttu-id="5466c-110">Erreur irrécupérable 216</span><span class="sxs-lookup"><span data-stu-id="5466c-110">Fatal Error 216</span></span>](#fatal-error-216)

[<span data-ttu-id="5466c-111">Erreur irrécupérable 217</span><span class="sxs-lookup"><span data-stu-id="5466c-111">Fatal Error 217</span></span>](#fatal-error-217)

[<span data-ttu-id="5466c-112">Erreur irrécupérable 218</span><span class="sxs-lookup"><span data-stu-id="5466c-112">Fatal Error 218</span></span>](#fatal-error-218)

[<span data-ttu-id="5466c-113">Erreur irrécupérable 219</span><span class="sxs-lookup"><span data-stu-id="5466c-113">Fatal Error 219</span></span>](#fatal-error-219)

[<span data-ttu-id="5466c-114">Erreur irrécupérable 220</span><span class="sxs-lookup"><span data-stu-id="5466c-114">Fatal Error 220</span></span>](#fatal-error-220)

## <a name="information-message-211"></a><span data-ttu-id="5466c-115">Message d’information 211</span><span class="sxs-lookup"><span data-stu-id="5466c-115">Information Message 211</span></span>

<dl> <dt>

<span data-ttu-id="5466c-116"><span id="_211__Information____Skipping_TRAP-TYPE__identifier__"></span><span id="_211__information____skipping_trap-type__identifier__"></span><span id="_211__INFORMATION____SKIPPING_TRAP-TYPE__IDENTIFIER__"></span>**<211, informations> : « interruption ignorée-TYPE <identifier> »**</span><span class="sxs-lookup"><span data-stu-id="5466c-116"><span id="_211__Information____Skipping_TRAP-TYPE__identifier__"></span><span id="_211__information____skipping_trap-type__identifier__"></span><span id="_211__INFORMATION____SKIPPING_TRAP-TYPE__IDENTIFIER__"></span>**<211, Information>: "Skipping TRAP-TYPE <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="5466c-117">Toutes les erreurs dans la définition TRAP-TYPE génèrent ce message.</span><span class="sxs-lookup"><span data-stu-id="5466c-117">Any errors in the TRAP-TYPE definition generate this message.</span></span>

</dd> </dl>

## <a name="fatal-error-212"></a><span data-ttu-id="5466c-118">Erreur irrécupérable 212</span><span class="sxs-lookup"><span data-stu-id="5466c-118">Fatal Error 212</span></span>

<dl> <dt>

<span data-ttu-id="5466c-119"><span id="_212__Fatal_____fileName___line____Syntax_Error_in_SEQUENCE_definition._Last_token_read_is__token__"></span><span id="_212__fatal_____filename___line____syntax_error_in_sequence_definition._last_token_read_is__token__"></span><span id="_212__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SEQUENCE_DEFINITION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<212,> irrécupérable : " <fileName> : <ligne \#> : erreur de syntaxe dans la définition de la séquence. La dernière lecture de jeton est <token> «**</span><span class="sxs-lookup"><span data-stu-id="5466c-119"><span id="_212__Fatal_____fileName___line____Syntax_Error_in_SEQUENCE_definition._Last_token_read_is__token__"></span><span id="_212__fatal_____filename___line____syntax_error_in_sequence_definition._last_token_read_is__token__"></span><span id="_212__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SEQUENCE_DEFINITION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<212, Fatal>: "<fileName>:<line\#>: Syntax Error in SEQUENCE definition. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="5466c-120">Erreur de syntaxe de module dans l’assignation de type.</span><span class="sxs-lookup"><span data-stu-id="5466c-120">Module syntax error in type assignment.</span></span> <span data-ttu-id="5466c-121">Il y a une erreur entre les accolades gauche et droite d’une construction de séquence, ce qui correspond à une erreur de syntaxe dans une affectation de type MIB.</span><span class="sxs-lookup"><span data-stu-id="5466c-121">There is an error between the left and right braces of a SEQUENCE construct, which amounts to a syntax error in a MIB type assignment.</span></span>

</dd> </dl>

## <a name="fatal-error-213"></a><span data-ttu-id="5466c-122">Erreur irrécupérable 213</span><span class="sxs-lookup"><span data-stu-id="5466c-122">Fatal Error 213</span></span>

<dl> <dt>

<span data-ttu-id="5466c-123"><span id="_213__Fatal_____fileName___line____Syntax_Error_in_Object_Identifier_value._Last_token_read_is__token__"></span><span id="_213__fatal_____filename___line____syntax_error_in_object_identifier_value._last_token_read_is__token__"></span><span id="_213__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_OBJECT_IDENTIFIER_VALUE._LAST_TOKEN_READ_IS__TOKEN__"></span>**<213,> irrécupérable : " <fileName> : <ligne \#> : erreur de syntaxe dans la valeur de l’identificateur d’objet. La dernière lecture de jeton est <token> «**</span><span class="sxs-lookup"><span data-stu-id="5466c-123"><span id="_213__Fatal_____fileName___line____Syntax_Error_in_Object_Identifier_value._Last_token_read_is__token__"></span><span id="_213__fatal_____filename___line____syntax_error_in_object_identifier_value._last_token_read_is__token__"></span><span id="_213__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_OBJECT_IDENTIFIER_VALUE._LAST_TOKEN_READ_IS__TOKEN__"></span>**<213, Fatal>: "<fileName>:<line\#>: Syntax Error in Object Identifier value. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="5466c-124">Erreur de syntaxe de module dans l’assignation de valeur.</span><span class="sxs-lookup"><span data-stu-id="5466c-124">Module syntax error in value assignment.</span></span> <span data-ttu-id="5466c-125">Il y a une erreur entre les accolades gauche et droite d’une valeur d’identificateur d’objet.</span><span class="sxs-lookup"><span data-stu-id="5466c-125">There is an error between the left and right braces of an object identifier value.</span></span>

</dd> </dl>

## <a name="fatal-error-214"></a><span data-ttu-id="5466c-126">Erreur irrécupérable 214</span><span class="sxs-lookup"><span data-stu-id="5466c-126">Fatal Error 214</span></span>

<dl> <dt>

<span data-ttu-id="5466c-127"><span id="_214__Fatal_____fileName___line____Syntax_Error_in_the_list_of_symbols_in_IMPORTS._Last_token_read_is__token__"></span><span id="_214__fatal_____filename___line____syntax_error_in_the_list_of_symbols_in_imports._last_token_read_is__token__"></span><span id="_214__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_LIST_OF_SYMBOLS_IN_IMPORTS._LAST_TOKEN_READ_IS__TOKEN__"></span>**<214,> irrécupérable : " <fileName> : <ligne \#> : erreur de syntaxe dans la liste de symboles dans les importations. La dernière lecture de jeton est <token> «**</span><span class="sxs-lookup"><span data-stu-id="5466c-127"><span id="_214__Fatal_____fileName___line____Syntax_Error_in_the_list_of_symbols_in_IMPORTS._Last_token_read_is__token__"></span><span id="_214__fatal_____filename___line____syntax_error_in_the_list_of_symbols_in_imports._last_token_read_is__token__"></span><span id="_214__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_LIST_OF_SYMBOLS_IN_IMPORTS._LAST_TOKEN_READ_IS__TOKEN__"></span>**<214, Fatal>: "<fileName>:<line\#>: Syntax Error in the list of symbols in IMPORTS. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="5466c-128">Erreur de syntaxe de module dans la section Imports.</span><span class="sxs-lookup"><span data-stu-id="5466c-128">Module syntax error in the IMPORTS section.</span></span>

</dd> </dl>

## <a name="fatal-error-215"></a><span data-ttu-id="5466c-129">Erreur irrécupérable 215</span><span class="sxs-lookup"><span data-stu-id="5466c-129">Fatal Error 215</span></span>

<dl> <dt>

<span data-ttu-id="5466c-130"><span id="_215__Fatal_____fileName___line____Syntax_Error_in_IMPORTS__missing_module_name__._Last_token_read_is__token__"></span><span id="_215__fatal_____filename___line____syntax_error_in_imports__missing_module_name__._last_token_read_is__token__"></span><span id="_215__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_IMPORTS__MISSING_MODULE_NAME__._LAST_TOKEN_READ_IS__TOKEN__"></span>**<215,> irrécupérable : " <fileName> : <ligne \#> : erreur de syntaxe dans Imports (nom de module manquant ?). La dernière lecture de jeton est <token> «**</span><span class="sxs-lookup"><span data-stu-id="5466c-130"><span id="_215__Fatal_____fileName___line____Syntax_Error_in_IMPORTS__missing_module_name__._Last_token_read_is__token__"></span><span id="_215__fatal_____filename___line____syntax_error_in_imports__missing_module_name__._last_token_read_is__token__"></span><span id="_215__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_IMPORTS__MISSING_MODULE_NAME__._LAST_TOKEN_READ_IS__TOKEN__"></span>**<215, Fatal>: "<fileName>:<line\#>: Syntax Error in IMPORTS (missing module name?). Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="5466c-131">Erreur de syntaxe de module dans la section Imports.</span><span class="sxs-lookup"><span data-stu-id="5466c-131">Module syntax error in the IMPORTS section.</span></span>

</dd> </dl>

## <a name="fatal-error-216"></a><span data-ttu-id="5466c-132">Erreur irrécupérable 216</span><span class="sxs-lookup"><span data-stu-id="5466c-132">Fatal Error 216</span></span>

<dl> <dt>

<span data-ttu-id="5466c-133"><span id="_216__Fatal_____fileName___line____Syntax_Error_in_the_IMPORTS_section._Last_token_read_is__token__"></span><span id="_216__fatal_____filename___line____syntax_error_in_the_imports_section._last_token_read_is__token__"></span><span id="_216__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_IMPORTS_SECTION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<216,> irrécupérable : " <fileName> : <ligne \#> : erreur de syntaxe dans la section Imports. La dernière lecture de jeton est <token> «**</span><span class="sxs-lookup"><span data-stu-id="5466c-133"><span id="_216__Fatal_____fileName___line____Syntax_Error_in_the_IMPORTS_section._Last_token_read_is__token__"></span><span id="_216__fatal_____filename___line____syntax_error_in_the_imports_section._last_token_read_is__token__"></span><span id="_216__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_IMPORTS_SECTION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<216, Fatal>: "<fileName>:<line\#>: Syntax Error in the IMPORTS section. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="5466c-134">Erreur de syntaxe de module dans la section Imports.</span><span class="sxs-lookup"><span data-stu-id="5466c-134">Module syntax error in the IMPORTS section.</span></span>

</dd> </dl>

## <a name="fatal-error-217"></a><span data-ttu-id="5466c-135">Erreur irrécupérable 217</span><span class="sxs-lookup"><span data-stu-id="5466c-135">Fatal Error 217</span></span>

<dl> <dt>

<span data-ttu-id="5466c-136"><span id="_217__Fatal_____fileName___line____Syntax_error_in_INTEGER_Enumeration._Last_token_read_is__token__"></span><span id="_217__fatal_____filename___line____syntax_error_in_integer_enumeration._last_token_read_is__token__"></span><span id="_217__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_INTEGER_ENUMERATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<217,> irrécupérable : " <fileName> : <ligne \#> : erreur de syntaxe dans l’énumération d’entier. La dernière lecture de jeton est <token> «**</span><span class="sxs-lookup"><span data-stu-id="5466c-136"><span id="_217__Fatal_____fileName___line____Syntax_error_in_INTEGER_Enumeration._Last_token_read_is__token__"></span><span id="_217__fatal_____filename___line____syntax_error_in_integer_enumeration._last_token_read_is__token__"></span><span id="_217__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_INTEGER_ENUMERATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<217, Fatal>: "<fileName>:<line\#>: Syntax error in INTEGER Enumeration. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="5466c-137">Toute erreur de syntaxe de module entre les accolades gauche et droite d’une définition d’énumération MIB génère ce message.</span><span class="sxs-lookup"><span data-stu-id="5466c-137">Any module syntax error between the left and right braces of a MIB enumeration definition generates this message.</span></span>

</dd> </dl>

## <a name="fatal-error-218"></a><span data-ttu-id="5466c-138">Erreur irrécupérable 218</span><span class="sxs-lookup"><span data-stu-id="5466c-138">Fatal Error 218</span></span>

<dl> <dt>

<span data-ttu-id="5466c-139"><span id="_218__Fatal_____fileName___line____Syntax_Error_in_sub-type_specification._Last_token_read_is__token__"></span><span id="_218__fatal_____filename___line____syntax_error_in_sub-type_specification._last_token_read_is__token__"></span><span id="_218__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SUB-TYPE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<218,> irrécupérable : " <fileName> : <ligne \#> : erreur de syntaxe dans la spécification de sous-type. La dernière lecture de jeton est <token> «**</span><span class="sxs-lookup"><span data-stu-id="5466c-139"><span id="_218__Fatal_____fileName___line____Syntax_Error_in_sub-type_specification._Last_token_read_is__token__"></span><span id="_218__fatal_____filename___line____syntax_error_in_sub-type_specification._last_token_read_is__token__"></span><span id="_218__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SUB-TYPE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<218, Fatal>: "<fileName>:<line\#>: Syntax Error in sub-type specification. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="5466c-140">Toute erreur de syntaxe de module entre les parenthèses dans une spécification de sous-type génère ce message.</span><span class="sxs-lookup"><span data-stu-id="5466c-140">Any module syntax error between the parentheses in a sub-type specification generates this message.</span></span>

</dd> </dl>

## <a name="fatal-error-219"></a><span data-ttu-id="5466c-141">Erreur irrécupérable 219</span><span class="sxs-lookup"><span data-stu-id="5466c-141">Fatal Error 219</span></span>

<dl> <dt>

<span data-ttu-id="5466c-142"><span id="_219__Fatal____fileName___line____Syntax_Error_in_the_SIZE_specification._Last_token_read_is__token__"></span><span id="_219__fatal____filename___line____syntax_error_in_the_size_specification._last_token_read_is__token__"></span><span id="_219__FATAL____FILENAME___LINE____SYNTAX_ERROR_IN_THE_SIZE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<219,> irrécupérable : " <fileName> : <ligne \#> : erreur de syntaxe dans la spécification de taille. La dernière lecture de jeton est <token> «**</span><span class="sxs-lookup"><span data-stu-id="5466c-142"><span id="_219__Fatal____fileName___line____Syntax_Error_in_the_SIZE_specification._Last_token_read_is__token__"></span><span id="_219__fatal____filename___line____syntax_error_in_the_size_specification._last_token_read_is__token__"></span><span id="_219__FATAL____FILENAME___LINE____SYNTAX_ERROR_IN_THE_SIZE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<219, Fatal>:"<fileName>:<line\#>: Syntax Error in the SIZE specification. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="5466c-143">Toute erreur de syntaxe de module dans la clause SIZE entre les parenthèses gauche et droite génère ce message.</span><span class="sxs-lookup"><span data-stu-id="5466c-143">Any module syntax error in the SIZE clause between the left and right parentheses generates this message.</span></span>

</dd> </dl>

## <a name="fatal-error-220"></a><span data-ttu-id="5466c-144">Erreur irrécupérable 220</span><span class="sxs-lookup"><span data-stu-id="5466c-144">Fatal Error 220</span></span>

<dl> <dt>

<span data-ttu-id="5466c-145"><span id="_220__Fatal____fileName___line____OBJECT-TYPE_invocation_of_SNMPv2SMI_not_allowed_"></span><span id="_220__fatal____filename___line____object-type_invocation_of_snmpv2smi_not_allowed_"></span><span id="_220__FATAL____FILENAME___LINE____OBJECT-TYPE_INVOCATION_OF_SNMPV2SMI_NOT_ALLOWED_"></span>**<220,> fatale : " <fileName> : <\#> de ligne : appel de type objet de SNMPv2SMI non autorisé"**</span><span class="sxs-lookup"><span data-stu-id="5466c-145"><span id="_220__Fatal____fileName___line____OBJECT-TYPE_invocation_of_SNMPv2SMI_not_allowed_"></span><span id="_220__fatal____filename___line____object-type_invocation_of_snmpv2smi_not_allowed_"></span><span id="_220__FATAL____FILENAME___LINE____OBJECT-TYPE_INVOCATION_OF_SNMPV2SMI_NOT_ALLOWED_"></span>**<220, Fatal>:"<fileName>:<line\#>: OBJECT-TYPE invocation of SNMPv2SMI not allowed"**</span></span>
</dt> <dd>

<span data-ttu-id="5466c-146">Erreur de syntaxe du module.</span><span class="sxs-lookup"><span data-stu-id="5466c-146">Module syntax error.</span></span> <span data-ttu-id="5466c-147">Vous avez utilisé l’appel de **type objet** spécifique à SNMPv2C dans la MIB, mais vous avez spécifié le commutateur **/v1** , qui requiert une conformité stricte à la syntaxe SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="5466c-147">You have used the SNMPv2C-specific **OBJECT-TYPE** invocation in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

 

 



