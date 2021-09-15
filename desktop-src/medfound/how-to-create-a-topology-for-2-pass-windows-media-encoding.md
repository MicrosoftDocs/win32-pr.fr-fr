---
description: les modes d’encodage en deux passes sont pris en charge par certains encodeurs Windows Media et Media Foundation au niveau de la couche de pipeline.
ms.assetid: 3fd5baff-142f-453e-bb97-b355ee6678fc
title: comment créer une topologie pour Two-Pass l’encodage de média Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c813b9a3c31fafaa3efbea83180c997bc46079d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413045"
---
# <a name="how-to-create-a-topology-for-two-pass-windows-media-encoding"></a>comment créer une topologie pour Two-Pass l’encodage de média Windows

les modes d’encodage en deux passes sont pris en charge par certains encodeurs Windows Media et Media Foundation au niveau de la couche de pipeline. L’application doit configurer et configurer la topologie d’encodage de la même manière que dans l’encodage à passage unique, mais en mode d’encodage en 2 passes, l’application doit exécuter la session d’encodage à deux reprises. Lors du premier passage, l’encodeur recueille des informations sur le contenu du flux. Lors de la deuxième passe, en utilisant les informations collectées lors du premier passage, le fichier de sortie final est généré. En traitant les exemples du flux à deux reprises, l’encodage en deux passes optimise le processus d’encodage et produit des fichiers encodés de qualité supérieure. Les modes d’encodage à deux passes ne peuvent pas être utilisés sur des flux dynamiques.

Media Foundation prend en charge les modes d’encodage à deux passes suivants :

-   [Encodage de la vitesse de transmission variable sans contrainte](unconstrained-variable-bit-rate--vbr--encoding.md)
-   [Chiffrement à vitesse de transmission variable à forte limite](peak-constrained-variable-bit-rate--vbr--encoding.md)

La création d’une topologie d’encodage pour l’encodage en deux passes est similaire aux modes de passe unique. La liste suivante présente les principales différences.

-   La configuration de l’encodeur doit inclure la propriété [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md) qui a la valeur 2 et la propriété [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) la \_ valeur variant true. Cela permet de filtrer les fonctionnalités de l’encodeur en modes à deux passes. Si vous utilisez des objets d’activation, transmettez ces propriétés à [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) ou [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).
-   Pour la première passe, utilisez un récepteur de médias factices dans le nœud de sortie, car les exemples générés dans ce test ne sont pas ajoutés au fichier final.
-   Pour la deuxième passe, interrogez l’encodeur pour les propriétés de recodage requises et remplacez le nœud du récepteur de média factice par le récepteur de média ASF avec les propriétés définies.

pour plus d’informations sur la configuration d’une topologie d’encodage, consultez [didacticiel : simple passe Windows encodage de média](tutorial--1-pass-windows-media-encoding.md).

la procédure suivante résume les étapes à suivre pour encoder Windows contenu multimédia dans un conteneur ASF à l’aide d’un mode d’encodage en deux passes.

1.  Créer une source de média pour le spécifié à l’aide du programme de résolution source.
2.  Énumérer les flux dans la source du média.
3.  Créez le récepteur de média ASF et ajoutez des récepteurs de flux en fonction des flux de la source du média qui doivent être encodés.
4.  Créez le récepteur multimédia.
5.  créez les encodeurs de média Windows pour les flux dans le fichier de sortie.
6.  Configurez les encodeurs avec les propriétés d’encodage à 2 passes.
7.  Générez une topologie d’encodage partielle en connectant la source, les encodeurs et le récepteur multimédia.
8.  Instanciez la session multimédia et définissez la topologie sur la session multimédia.
9.  Exécutez la première passe d’encodage en contrôlant la session multimédia et en obtenant tous les événements pertinents à partir de la session multimédia.
10. Fermez et arrêtez la session d’encodage.
11. Interrogez l’encodeur pour les propriétés suivantes selon le type d’encodage : 

    | Type d’encodage                                                                                        | Nom de la propriété                                                                                                                                                                                                                                                                                                                                                     |
    |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [Encodage de la vitesse de transmission variable sans contrainte](unconstrained-variable-bit-rate--vbr--encoding.md)       | [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)<br/> [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)<br/> [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)<br/> [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md)<br/>                                                                                                               |
    | [Chiffrement à vitesse de transmission variable à forte limite](peak-constrained-variable-bit-rate--vbr--encoding.md) | [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)<br/> [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)<br/> [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)<br/> [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md)<br/> [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md)<br/> [**MFPKEY \_ Rmax**](mfpkey-rmaxproperty.md)<br/> |

    

     

12. Créez le récepteur de fichiers ASF et ajoutez les récepteurs de flux requis en fonction des flux que vous souhaitez inclure dans le fichier de sortie final.
13. Définissez les propriétés de l’encodeur récupérées à l’étape 11 sur le récepteur de fichiers.
14. Remplacez le récepteur multimédia du nœud de sortie par le récepteur de fichiers nouvellement créé.
15. Instanciez la session multimédia et définissez la topologie mise à jour sur la session de média.
16. Exécutez la deuxième passe d’encodage en contrôlant la session multimédia et en obtenant tous les événements pertinents à partir de la session multimédia.
17. Attendez que l’événement [MEEndOfPresentation](meendofpresentation.md) de la session multimédia et dans le gestionnaire d’événements récupère les valeurs de propriété d’encodage de l’encodeur et définissez-les sur le récepteur de fichiers. pour plus d’informations, consultez « mettre à jour les propriétés d’encodage dans le récepteur de fichiers » dans le [didacticiel : simple passe Windows encodage de média](tutorial--1-pass-windows-media-encoding.md).
18. Fermez et arrêtez la session d’encodage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Composants ASF de couche de pipeline](pipeline-layer-asf-components.md)
</dt> </dl>

 

 




