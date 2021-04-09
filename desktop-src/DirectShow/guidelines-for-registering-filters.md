---
description: Instructions pour l’enregistrement des filtres
ms.assetid: 05945937-9e01-4930-ae95-1931a711b55e
title: Instructions pour l’enregistrement des filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed616d90c17d232995994d8ceccfdc72d022d56
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108434"
---
# <a name="guidelines-for-registering-filters"></a>Instructions pour l’enregistrement des filtres

Les informations du registre de filtre déterminent la façon dont le gestionnaire de graphes de filtre fonctionne pendant la [connexion intelligente](intelligent-connect.md). Par conséquent, il affecte toutes les applications écrites pour DirectShow, pas seulement celles qui utiliseront votre filtre. Vous devez vous assurer que votre filtre se comporte correctement, en suivant ces instructions.

1.  Avez-vous besoin des données de filtre dans le registre ? Pour de nombreux filtres personnalisés, il n’y a aucune raison de rendre le filtre visible pour le mappeur de filtre ou l’énumérateur du périphérique système. Tant que vous inscrivez la DLL, votre application peut créer le filtre à l’aide de **CoCreateInstance**. Dans ce cas, omettez simplement la structure de [**\_ filtre AMOVIESETUP**](amoviesetup-filter.md) dans le modèle de fabrique. (L’un des inconvénients est que votre filtre ne sera pas visible dans GraphEdit. Pour contourner ce problèmes, vous pouvez créer une catégorie « test » privée à l’aide de la méthode [**IFilterMapper2 :: CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory) . Vous ne devez effectuer cette opération que pour les versions Debug.)
2.  Choisissez la catégorie de filtre correcte. La catégorie « filtres DirectShow » par défaut est pour les filtres à usage général. Le cas échéant, inscrivez votre filtre dans une catégorie plus spécifique. Quand [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) recherche un filtre, il ignore toute catégorie dont la mérite n’est \_ \_ pas \_ utilisée ou moins. Les catégories non destinées à la lecture normale ont une faible mérite.
3.  Évitez de spécifier MEDIATYPE \_ None, MEDIASUBTYPE \_ None ou GUID \_ null dans les informations de [**\_ MediaType AMOVIESETUP**](amoviesetup-mediatype.md) pour un code confidentiel. **IFilterMapper2** les traite comme des caractères génériques, ce qui peut ralentir le processus de création de graphiques.
4.  Choisissez la valeur de mérite la plus faible possible. Voici quelques recommandations :

    | Type de filtre                                                                                       | Mérite recommandée                                                                                   |
    |------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
    | Convertisseur par défaut                                                                                     | \_préférence mérite. Toutefois, pour les types de média standard, un convertisseur personnalisé ne doit jamais être la valeur par défaut. |
    | Convertisseur autre que celui par défaut                                                                                 | Les MÉRITEs \_ n' \_ \_ utilisent pas ou ne méritent pas de \_ chances                                                              |
    | Mux                                                                                                  | MÉRITE \_ n' \_ \_ utilise pas                                                                                 |
    | Décodeur                                                                                              | MÉRITE \_ normal                                                                                       |
    | Spitter, analyseur                                                                                      | MÉRITE \_ normal ou Lower                                                                              |
    | Filtre à usage spécial ; tout filtre créé directement par l’application                       | MÉRITE \_ n' \_ \_ utilise pas                                                                                 |
    | Capture                                                                                              | MÉRITE \_ n' \_ \_ utilise pas                                                                                 |
    | Filtre « de secours »; par exemple, le [filtre de convertisseur d’espace colorimétrique](color-space-converter-filter.md) | MÉRITE \_ improbable                                                                                     |

    

     

    Si vous donnez à un filtre un mérite de mérite \_ \_ , n' \_ utilisez pas, déterminez si vous devez enregistrer ces informations en premier lieu. (Voir l’élément 1.)

5.  N’inscrivez pas de filtre dans la catégorie « filtres DirectShow » qui accepte les couleurs RVB 24 bits. Votre filtre interfère avec le filtre de convertisseur d’espace de couleurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



