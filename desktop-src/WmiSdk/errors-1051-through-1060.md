---
description: Décrit les erreurs du fournisseur SNMP WMI 1051 à 1060.
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: Erreurs 1051 à 1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3405a799d71b33fa1dabd7c84964b8d1726d2e27
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882585"
---
# <a name="errors-1051-through-1060"></a>Erreurs 1051 à 1060

Décrit les erreurs du fournisseur SNMP WMI 1051 à 1060.

[Erreur irrécupérable 1051](#fatal-error-1051)

[Erreur irrécupérable 1054](#fatal-error-1054)

[Erreur irrécupérable 1055](#fatal-error-1055)

## <a name="fatal-error-1051"></a>Erreur irrécupérable 1051

<dl> <dt>

<span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051,> fatale : " &lt; filename &gt; : <Line \#> : référence ambiguë à l’identificateur de symbole &lt; &gt; "**
</dt> <dd>

Erreur de sémantique du module d’importation, propre à SNMPv1 et SNMPv2C. Chaque descripteur d’objet correspondant à un objet dans une MIB Internet standard doit être unique. Étant donné que les MIB d’entreprise peuvent avoir des descripteurs d’objets communs, ces descripteurs importés à partir de deux modules doivent être utilisés sans ambiguïté dans le module MIB à l’aide de la notation « module. Descriptor ».

</dd> </dl>

## <a name="fatal-error-1054"></a>Erreur irrécupérable 1054

<dl> <dt>

<span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054,> irrécupérable : " &lt; filename &gt; : <Line \#> : l' &lt; identificateur &gt; dans la clause d’index n’est pas résolu en l’un des types autorisés"**
</dt> <dd>

Erreur sémantique du module d’appel **de macro de type objet** . Le type d’un objet dans la clause d’INDEX, ou tout type spécifié dans la clause d’INDEX, doit correspondre à un type scalaire, c’est-à-dire à une séquence ou non de type. Tout type spécifié dans la clause INDEX doit également être résolu en l’un de ces types.

Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1055"></a>Erreur irrécupérable 1055

<dl> <dt>

<span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055,> fatale : " &lt; filename &gt; : <Line \#> : syntax of index Object-type &lt; identifier &gt; , n’est pas résolu en l’un des types autorisés"**
</dt> <dd>

Erreur sémantique du module d’appel **de macro de type objet** . Le type d’un objet dans la clause d’INDEX, ou tout type spécifié dans la clause d’INDEX, doit correspondre à un type scalaire, c’est-à-dire à une séquence ou non de type.

Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.

</dd> </dl>

 

 



