---
description: Le terme &\# 0034 ; language&\# 0034 ; indique une collection de propriétés utilisées dans des communications orales et écrites.
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: Paramètres régionaux et langues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2c0d0fa41b9186b2135d9497d52de24577bbae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524930"
---
# <a name="locales-and-languages"></a>Paramètres régionaux et langues

Le terme « langue » indique une collection de propriétés utilisées dans des communications orales et écrites. Chaque langue a un nom de langue et un identificateur de langue qui indiquent la [page de codes](code-pages.md) particulière (ANSI, dos, Macintosh) utilisée pour représenter l' [emplacement géographique](table-of-geographical-locations.md) de la langue sur le système d’exploitation. Une langue neutre est indiquée par un nom tel que « en » pour l’anglais. Une langue plus spécifique à chaque graphique peut être indiquée par un nom qui comprend des informations sur les paramètres régionaux et les pays/région. Par exemple, les paramètres régionaux anglais (États-Unis) ont le nom de langue « en-US ».

Les paramètres régionaux sont une collection d’informations de préférences d’utilisateur liées à la langue, représentées sous la forme d’une liste de valeurs. Windows XP prend en charge plus de 150 de paramètres régionaux et Windows Vista prend en charge environ 200. Chaque paramètre régional est défini par une langue et un ordre de tri, et a à la fois un nom de paramètres régionaux et un identificateur de paramètres régionaux. Un exemple de nom de paramètres régionaux pour l’allemand (Allemagne) est « de-DE- \_ Phonebook ».

Chaque système d’exploitation a au moins un paramètre régional installé et a souvent plusieurs paramètres régionaux à partir desquels l’utilisateur peut les sélectionner. Chaque paramètre régional a une variété d’informations qui lui sont associées, à l’exception de son nom et de son identificateur. Les types d’informations de paramètres régionaux sont décrits dans [constantes d’informations de paramètres régionaux](locale-information-constants.md).

Le système d’exploitation attribue des paramètres régionaux à chaque thread, en affectant initialement les « paramètres régionaux par défaut du système » définis par la [ \_ \_ valeur par défaut du système de paramètres régionaux](locale-system-default.md). Ces paramètres régionaux sont définis lors de l’installation du système d’exploitation ou lorsque l’utilisateur le sélectionne à l’aide de la section Options régionales et linguistiques du panneau de configuration. Lors de l’exécution d’un thread dans un processus appartenant à l’utilisateur, le système d’exploitation affecte les « paramètres régionaux par défaut de l’utilisateur » au thread. Ces paramètres régionaux sont définis par les paramètres [régionaux \_ \_ par défaut](locale-user-default.md)de l’utilisateur. Une application peut remplacer l’option par défaut à l’aide de la fonction [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) pour définir explicitement les paramètres régionaux d’un thread.

L’implémentation d’un langage requiert des paramètres régionaux correspondants. Le système d’exploitation implémente une langue neutre en sélectionnant les données pour les paramètres régionaux associés à une version spécifique de la langue, généralement les paramètres régionaux les plus répandus.

À compter de Windows Vista, il est possible qu’une langue particulière corresponde à des paramètres régionaux supplémentaires, qui est un type de paramètres régionaux personnalisés. Étant donné que les paramètres régionaux supplémentaires partagent tous un identificateur de paramètres régionaux unique, vos applications doivent gérer ces paramètres régionaux et les langues correspondantes par leur nom plutôt que par leur identificateur.

Les concepts de langage sont étroitement liés aux concepts des paramètres régionaux, mais les deux termes ne sont pas interchangeables. En règle générale, les fonctions liées à l' [interface utilisateur multilingue](multilingual-user-interface.md) concernent les langues, tandis que les fonctions nls agissent sur les paramètres régionaux.

Les rubriques traitées dans cette section sont les suivantes :

-   [Paramètres régionaux personnalisés](custom-locales.md)
-   [Identificateurs de langue](language-identifiers.md)
-   [Noms des langues](language-names.md)
-   [Identificateurs de paramètres régionaux](locale-identifiers.md)
-   [Noms de paramètres régionaux](locale-names.md)
-   [Pseudo-paramètres régionaux](pseudo-locales.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la prise en charge linguistique nationale](about-national-language-support.md)
</dt> <dt>

[Pages de codes](code-pages.md)
</dt> <dt>

[Constantes d’informations de paramètres régionaux](locale-information-constants.md)
</dt> <dt>

[Interface utilisateur multilingue](multilingual-user-interface.md)
</dt> <dt>

[Tableau des zones géographiques](table-of-geographical-locations.md)
</dt> <dt>

[Gestion de la langue de l’interface utilisateur](user-interface-language-management.md)
</dt> <dt>

[**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



