---
title: Paramètres du registre du schéma personnalisé
description: Paramètres du registre du schéma personnalisé
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Lecteur Windows Media, paramètres de registre du schéma personnalisé
- Lecteur Windows Media, schémas
- Lecteur Windows Media, registre
- Registre, paramètres de schéma personnalisés
- Registre, schémas
- registre, paramètres pour Lecteur Windows Media
- schémas
- paramètres de Registre du schéma personnalisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a02649d9536140fff0ff0d3188a5b25feb49688
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228521"
---
# <a name="custom-scheme-registry-settings"></a>Paramètres du registre du schéma personnalisé

Les schémas sont des protocoles personnalisés. Lecteur Windows Media gère une liste de schémas dans le registre sur l’ordinateur de l’utilisateur. lorsque l’utilisateur tente de lire un fichier multimédia numérique, le lecteur vérifie d’abord si le kit de développement logiciel (SDK) Windows media Format prend en charge le schéma. Si ce n’est pas le cas, le lecteur vérifie le schéma par rapport à la liste figurant dans le registre. si une correspondance est trouvée, le lecteur vérifie ensuite une valeur qui indique la technologie sous-jacente ou le *runtime* (par exemple, Microsoft DirectShow ou le kit de développement logiciel (SDK) Windows Media Format), qui peut être utilisé pour lire le fichier. Si aucune correspondance n’est trouvée, le lecteur présente à l’utilisateur une boîte de dialogue d’avertissement qui demande à l’utilisateur l’autorisation d’essayer de lire le fichier. Si vous diffusez en continu des fichiers multimédias numériques à l’aide d’un schéma de protocole personnalisé, vous pouvez empêcher l’affichage de cet avertissement sur l’ordinateur de l’utilisateur en inscrivant le schéma et en fournissant une valeur pour le Runtime.

La liste des schémas est conservée sous la forme d’un ensemble de clés de Registre qui correspondent aux schémas inscrits, sans le signe deux-points et les deux barres obliques (://). Par exemple, la clé pour le schéma wmhtml://, qui est utilisé pour diffuser des médias enrichis, est nommée « wmhtml ». Une liste distincte est conservée pour l’ordinateur local et pour chaque utilisateur. Pour l’ordinateur local, les clés de schéma sont des sous-clés de la clé de Registre suivante :

**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Multimedia pour les \\ \\ modèles wmplayer\\**

Par exemple, la clé du schéma wmhtml://pour l’ordinateur local est la suivante :

**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Multimedia \\ \\ wmhtml schemas \\**

Pour modifier les valeurs de cette clé ou pour créer une nouvelle sous-clé, l’utilisateur actuel doit être administrateur de l’ordinateur.

Pour les utilisateurs individuels, les clés de schéma sont des sous-clés de la clé de Registre suivante :

**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ MediaPlayer \\ Player \\ schemas\\**

Par exemple, la clé du schéma wmhtml://pour l’utilisateur actuel est :

**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ MediaPlayer \\ Player \\ schemas \\ wmhtml**

Lors de la vérification des schémas inscrits, le lecteur vérifie d’abord les valeurs situées dans **HKEY \_ local \_ machine**. Si aucune valeur n’est trouvée pour le schéma actuel, le lecteur vérifie ensuite les valeurs dans **HKEY \_ Current \_ User**. Si aucune valeur n’est trouvée pour le schéma actuel, le lecteur affiche l’avertissement à l’utilisateur.

Chaque sous-clé de schéma peut contenir l’une des valeurs possibles suivantes pour l' *exécution*.



| Valeur | Description                                |
|-------|--------------------------------------------|
| 6     | rendu à l’aide du kit de développement logiciel (SDK) Windows Media Format. |
| 7     | Effectuer un rendu à l’aide de Microsoft DirectShow.         |



 

la modification de la valeur d' *exécution* d’un schéma pris en charge par le kit de développement logiciel (SDK) Windows Media Format n’a aucun effet. le lecteur utilise toujours le kit de développement logiciel (sdk) de format de média Windows comme runtime pour les schémas pris en charge par le kit de développement logiciel (sdk) Windows media format. Cette valeur de Registre est conçue pour permettre la configuration du runtime pour les schémas personnalisés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres du Registre**](registry-settings.md)
</dt> </dl>

 

 




