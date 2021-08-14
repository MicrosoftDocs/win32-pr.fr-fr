---
description: 'Windows Vista et versions ultérieures : NLS définit plusieurs pseudo-paramètres régionaux à utiliser en plus des paramètres régionaux Windows existants.'
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e099ee2af283c38aff3de7813fec64b5d43c6ac5873549856b27fd224c3e0d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390413"
---
# <a name="pseudo-locales"></a>Pseudo-Locales

**Windows Vista et versions ultérieures :** NLS définit plusieurs pseudo-paramètres régionaux à utiliser en plus des paramètres régionaux Windows existants. Utilisez ces pseudo-paramètres régionaux pour tester la localisation de vos applications. Pour plus d’informations sur l’implémentation, consultez [utilisation de Pseudo-Locales pour le test de localisation](using-pseudo-locales-for-localization-testing.md).

## <a name="supported-pseudo-locales"></a>Pseudo-Locales pris en charge

Les pseudo-paramètres régionaux pris en charge par NLS sont les suivants :

-   Pseudo-paramètres régionaux de base
-   Pseudo-paramètres régionaux mis en miroir (de droite à gauche)
-   Pseudo-paramètres régionaux de langue orientale

Choisissez les pseudo-paramètres régionaux particuliers à utiliser en fonction de leurs affectations de pages de codes et des chaînes de localisation, par exemple, les noms de mois et les noms de jours. Les données pour chaque Pseudo-paramètres régionaux incluent non seulement les pages de code pertinentes et les chaînes de jour et de mois pour la localisation, mais également des données pour plusieurs autres cas de test pour NLS. Les cas de test examinent les types de données suivants :

-   [identificateurs de paramètres régionaux](locale-identifiers.md)9 bits. Les pseudo-paramètres régionaux offrent une bonne opportunité de tester le fonctionnement des identificateurs de paramètres régionaux 9 bits.
-   Chaînes de langues qui doivent utiliser de petites polices. En raison des limitations de l’interface GDI (Graphics Device Interface), la police de l’interface utilisateur pour certaines langues est plus petite que optimale. Les pseudo-paramètres régionaux incluent plusieurs chaînes de ces langages, combinées avec des chaînes de langages avec une gestion des polices plus standard. Vous pouvez utiliser ces chaînes dans le test pour déterminer comment une police limitée par GDI est restituée.
-   Longueurs de chaîne inhabituelles. Certaines constantes d’informations de paramètres régionaux, par exemple, les [paramètres régionaux \_ slist](locale-slist.md) et les [paramètres régionaux \_ ICURRENCY](locale-icurrency.md), ont des limites conventionnelles sur la taille de la chaîne. Les pseudo-paramètres régionaux prennent en charge l’examen des longueurs de chaîne variables.
-   Autres tris. Les pseudo-paramètres régionaux peuvent être utilisés pour tester les fonctionnalités de tri de remplacement lorsque l' [identificateur d’ordre de tri](sort-order-identifiers.md) de remplacement diffère de l’identificateur d’ordre de tri de base qui est généralement associé aux paramètres régionaux.

## <a name="pseudo-locale-names-and-identifiers"></a>Noms et identificateurs de Pseudo-paramètres régionaux

Les pseudo-paramètres régionaux ont des [noms de paramètres régionaux](locale-names.md) qui sont choisis à partir de l’espace d’utilisation privé pour éviter tout conflit avec les chaînes possibles introduites dans les normes Organisation internationale de normalisation (iso) 639 et ISO 3166. Chaque Pseudo-paramètres régionaux a également son propre identificateur de paramètres régionaux. Le tableau suivant fournit les noms et les identificateurs pour les pseudo-paramètres régionaux définis.



| Pseudo-paramètres régionaux       | Nom des paramètres régionaux | Identificateur de paramètres régionaux |
|---------------------|-------------|-------------------|
| Base                | RPS-Ploc    | 0501              |
| En miroir            | RPS-plocm   | 09ff              |
| Asie de l’est-langue | RPS-Ploca   | 05fe              |



 

## <a name="example"></a> Exemple

L’exemple suivant affiche le texte affiché pour les pseudo-paramètres régionaux de base :

\[Шěđлеśđαỳ !!! \] , 8 ōf \[ Μäŕςћ !! \] ōf 2006

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres régionaux et langues](locales-and-languages.md)
</dt> <dt>

[Identificateurs de paramètres régionaux](locale-identifiers.md)
</dt> <dt>

[Noms de paramètres régionaux](locale-names.md)
</dt> <dt>

[Identificateurs d’ordre de tri](sort-order-identifiers.md)
</dt> <dt>

[Utilisation de Pseudo-Locales pour le test de la localisation](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



