---
description: Décrit les erreurs du fournisseur SNMP WMI 1061 à 1070.
ms.assetid: 1bbd6153-7241-4673-ae17-1caa92b2e6a6
ms.tgt_platform: multiple
title: Erreurs 1061 à 1070
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7da7fb7eeacf9200e96890581766bfe31d9f19c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886854"
---
# <a name="errors-1061-through-1070"></a>Erreurs 1061 à 1070

Décrit les erreurs du fournisseur SNMP WMI 1061 à 1070.

[Erreur irrécupérable 1063](#fatal-error-1063)

[Erreur irrécupérable 1064](#fatal-error-1064)

[Erreur irrécupérable 1070](#fatal-error-1070)

## <a name="fatal-error-1063"></a>Erreur irrécupérable 1063

<dl> <dt>

<span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063,> irrécupérable : " &lt; nomfichier &gt;<ligne \#> : la limite supérieure de la spécification de taille est inférieure à la limite inférieure)**
</dt> <dd>

Erreur de sémantique de module dans la spécification de taille, propre à ni SNMPv1 ni SNMPv2C. Le symbole utilisé dans une spécification de taille doit être converti en OCTET STRING ou opaque. La limite inférieure d’une plage ou d’une spécification de taille ne doit pas être supérieure à la limite supérieure.

</dd> </dl>

## <a name="fatal-error-1064"></a>Erreur irrécupérable 1064

<dl> <dt>

<span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064,> irrécupérable : " &lt; NomFichier &gt; : <ligne \#> : &lt; l’identificateur d’élément &gt; de séquence ne se résout pas en type d’objet"**
</dt> <dd>

Erreur de sémantique du module d’assignation de type, propre à SNMPv1 et SNMPv2C. Tous les éléments individuels d’une déclaration de séquence doivent être résolus en un TYPE d’objet.

</dd> </dl>

## <a name="fatal-error-1070"></a>Erreur irrécupérable 1070

<dl> <dt>

<span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070,> fatale : " &lt; fileName &gt;<Line \#> : MIB module &lt; modulename &gt; , à partir duquel le symbole &lt; symbolName &gt; est importé, n’est pas présent dans l’entrée"**
</dt> <dd>

Erreur de sémantique de module dans le référence croisée, spécifique à, ou à SNMPv1 et à SNMPv2C. Si l’un des modules de la section Imports du module principal ou d’un module subsidiaire n’existe pas et qu’un ou plusieurs symboles de ce module sont réellement référencés, cette erreur irrécupérable se produit.

</dd> </dl>

 

 



