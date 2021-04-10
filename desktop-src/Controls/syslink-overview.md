---
title: À propos des contrôles SysLink
description: Un contrôle SysLink est une fenêtre qui affiche le texte marqué et notifie l’application quand les utilisateurs cliquent sur ses liens hypertexte incorporés. Ce contrôle offre une alternative pratique à l’utilisation du bouton de lien de commande. Pour plus d’informations, consultez types de boutons.
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb0d15cac479b844b0ea8510c34cc57f56822be
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031921"
---
# <a name="about-syslink-controls"></a>À propos des contrôles SysLink

Un contrôle SysLink est une fenêtre qui affiche le texte marqué et notifie l’application quand les utilisateurs cliquent sur ses liens hypertexte incorporés. Ce contrôle offre une alternative pratique à l’utilisation du [**bouton de lien de commande**](button-styles.md). Pour plus d’informations, consultez [types de boutons](button-types-and-styles.md).

Chaque contrôle SysLink peut prendre en charge plusieurs liens hypertexte et vous pouvez y accéder à l’aide d’un index de base zéro. Le contrôle SysLink est défini dans la version 6 du ComCtl32.dll, et il requiert un manifeste ou une directive qui spécifie que la version 6 de la DLL doit être utilisée si elle est disponible. Pour plus d’informations, consultez [activation des styles visuels](cookbook-overview.md).

Cet article contient les sections suivantes.

-   [Balisage SysLink](#syslink-markup)
-   [Attributs de lien](#link-attributes)
-   [États des liens](#link-states)
-   [Limitations relatives à l’affichage de texte bidirectionnel](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a>Balisage SysLink

Le contrôle SysLink prend en charge la balise d’ancrage ( &lt; a &gt; ), ainsi que les attributs **href** et **ID**. Un **href** peut être n’importe quel protocole, tel que http, FTP et mailto. Un **ID** est un nom facultatif, unique au sein d’un contrôle Syslink, et il est associé à un lien individuel. Les liens reçoivent également un index de base zéro en fonction de leur position dans la chaîne. Cet index est utilisé pour accéder à un lien.

## <a name="link-attributes"></a>Attributs de lien

Les attributs de chaque lien peuvent être définis dans la balise d’ancrage de chaque lien ou en envoyant le message [**LM \_ SETITEM**](lm-setitem.md) . La définition d’un attribut en le spécifiant dans la chaîne d’initialisation initialise simplement la valeur. Vous pouvez modifier la valeur d’un attribut par le biais de l’utilisation ultérieure du message **LM \_ SETITEM** .

## <a name="link-states"></a>États des liens

Les éléments de lien peuvent être dans l’un des trois États, représentés par les indicateurs dans le tableau suivant.



| Indicateur d’État   | Apparence et signification                                            |
|--------------|-------------------------------------------------------------------|
| actif \_ lis | Le lien a le focus clavier et appuyez sur entrée pour l’activer. |
| LIS \_ activé | Le lien est activé.                                              |
| LIS \_ visité | L’utilisateur a déjà visité l’URL représentée par le lien.     |



 

## <a name="limitations-on-bidirectional-text-display"></a>Limitations relatives à l’affichage de texte bidirectionnel

Certains langages, tels que l’arabe ou l’hébreu, sont écrits de droite à gauche (RTL); L’anglais est écrit de gauche à droite (LTR). La combinaison de RTL avec LTR est appelée texte bidirectionnel. Mélanger les constructions de balisage directionnelle LTR et RTL Unicode ou HTML dans les chaînes de ressources, en tant que marqueurs de déroulement bidirectionnel pour contrôler le workflow de chaînes, peut ne pas produire le résultat attendu lors de l’utilisation d’un contrôle SysLink. Par exemple, une phrase marquée LTR peut ne pas s’afficher correctement dans le contexte RTL.

> [!Note]  
> Les contrôles SysLink ne prennent pas en charge l’affichage bidirectionnel dans tous les scénarios. Utilisez un contrôle SysLink uniquement si vous savez qu’une disposition LTR ou RTL simple est appropriée. Sinon, envisagez d’utiliser une technologie plus avancée telle que [mshtml](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).

 

 

 