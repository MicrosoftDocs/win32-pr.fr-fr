---
description: Certaines valeurs utilisées avec les modules de fusion configurables nécessitent une gestion de texte spéciale.
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: Format spécial CMSM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8521c422d62980da0d222f8a8fc8395afa40b68bfd65c5600298372b1035f97d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252139"
---
# <a name="cmsm-special-format"></a>Format spécial CMSM

Certaines valeurs utilisées avec les modules de fusion configurables nécessitent une gestion de texte spéciale. Une chaîne de texte décrite comme étant dans « CMSM Special format » traite le point-virgule (;) et est égal à (=) caractères comme caractères réservés utilisés par l’outil de fusion du client ou Mergemod.dll.

Le format spécial CMSM est actuellement utilisé aux emplacements suivants :

-   Colonne de ligne de la [table ModuleSubstitution](modulesubstitution-table.md).
-   Colonne de valeur de la [table ModuleSubstitution](modulesubstitution-table.md).
-   La colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md) lorsque le champ de valeurs par champ est la valeur dans la colonne format.
-   La colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md) lorsque Text est la valeur dans la colonne format et enum est la valeur dans la colonne Type.
-   Colonne DefaultValue de la [table ModuleConfiguration](moduleconfiguration-table.md) lorsque key est la valeur de la colonne format.
-   Éléments configurables dans le format de clé utilisé par la [**méthode ProvideTextData**](configuremodule-providetextdata.md).

Pour entrer des points-virgules littéraux ou des caractères équivalents dans une valeur au format spécial CMSM, faites précéder le caractère d’une barre oblique inverse (« \\ »). Une barre oblique inverse littérale peut être représentée par deux barres obliques inverses. Un caractère unique préfixé par une barre oblique inverse unique est converti en caractère unique, même si l’échappement du caractère n’est pas nécessaire.

Si un point-virgule ou un caractère égal n’est pas précédé d’une barre oblique inverse mais qu’il n’a pas encore de comportement défini dans le contexte de la valeur, la chaîne résultante n’est pas définie. Par exemple, la colonne DefaultValue de la table ModuleConfiguration est au format spécial CMSM pour tous les éléments clés, car le point-virgule est le délimiteur de colonne. Bien que le caractère égal n’ait aucune signification particulière dans cette chaîne, les caractères littéraux doivent toujours être placés dans une séquence d’échappement dans cette chaîne.

 

 



