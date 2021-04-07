---
description: Paramètres de champ DVINFO dans le pilote MSDV
ms.assetid: f0723da5-4f53-4f83-a657-ae42815a784e
title: Paramètres de champ DVINFO dans le pilote MSDV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4205a680833b0e2f8c6be2dc4cb65faa60515867
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746668"
---
# <a name="dvinfo-field-settings-in-the-msdv-driver"></a>Paramètres de champ DVINFO dans le pilote MSDV

Cette section décrit comment le pilote MSDV remplit la structure [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .

La `DVINFO` structure définit le bloc de format pour les connexions de code confidentiel entre MSDV et d’autres filtres. Par défaut, le filtre de séparateur DV est utilisé lors de la capture à partir d’un périphérique DV et le filtre MUX DV est utilisé lors de la transmission à l’appareil. Toutefois, les applications peuvent fournir leurs propres filtres personnalisés. il est donc utile de comprendre comment MSDV remplit le `DVINFO` bloc de format.

La `DVINFO` structure contient les informations suivantes :

-   Deux packs sources audio auxiliaires (AAUX) pour les premier et deuxième blocs audio.
-   Deux packs de contrôle de code source AAUX pour les premier et deuxième blocs audio.
-   Un pack source VAUX (Video auxiliaire).
-   Un pack de contrôle de code source VAUX.

Chaque trame dans un flux DV contient des packs AAUX et VAUX. Toutefois, le `DVINFO` bloc de format est statique et n’est utilisé que pour établir la connexion de code confidentiel. Lorsque le pilote MSDV se connecte, il n’examine pas les packs AAUX ou VAUX dans le flux. Au lieu de cela, il utilise un ensemble de valeurs par défaut, en fonction des caractéristiques suivantes du périphérique DV :

-   Si l’appareil prend en charge un format de consommateur (magnétoscope) ou un format professionnel (DVCPRO)
-   Type de signal
-   Indique si le format est NTSC ou PAL. (Si l’appareil ne signale pas ces informations, MSDV utilise par défaut les paramètres NTSC)

Une fois que la diffusion en continu commence, il est de la responsabilité des filtres en mode utilisateur, tels que le séparateur DV, d’examiner le contenu réel de chaque image DV. Comme les informations peuvent changer d’une image à l’autres, il se peut que le filtre doive effectuer une modification de format dynamique. Par exemple, si le débit audio change, il se peut que le filtre doive renégocier le type audio.

Si vous capturez un fichier DV de type 1, la `DVINFO` structure est écrite dans le fichier en tant que bloc de format de flux ('Strf'). Ces données sont extraites directement du bloc de format fourni par MSDV. Comme indiqué, le contenu réel du flux peut être différent. Il incombe à l’application d’examiner les AAUX et les packs VAUX dans chaque frame.

Dans les rubriques suivantes, vous pouvez trouver des tables qui répertorient tous les champs utilisés par MSDV.

-   [Pack source AAUX (AS)](aaux-source--as--pack.md)
-   [Pack de contrôle de code source AAUX (ASC)](aaux-source-control--asc--pack.md)
-   [Pack source VAUX (VS)](vaux-source--vs--pack.md)
-   [Pack de contrôle de code source VAUX (VSC)](vaux-source-control--vsc--pack.md)

Lors de la lecture de ces tables, consultez les spécifications suivantes :

-   IEC 61834
-   314M SMPTE
-   SMPTE 370

Dans chaque table, la première colonne indique le code de champ, suivi du nombre de bits (entre parenthèses). Les colonnes restantes fournissent les valeurs de champ. La plupart des champs AAUX et VAUX ne sont pas pertinents pour la connexion de code confidentiel, auquel cas MSDV définit une valeur factice. La valeur numérique de l’ensemble du Pack est indiquée au bas de chaque table.

Les remarques après chaque tableau fournissent des informations supplémentaires sur les champs sélectionnés. Pour obtenir une description complète, reportez-vous aux spécifications. En outre, certains champs n’ont pas la même signification dans SMPTE 314M/SMPTE 370 que dans IEC 61834.

> [!Note]  
> Actuellement, DirectShow ne prend pas en charge les formats DVCPRO. Les valeurs répertoriées pour les formats DVCPRO sont définies pour une utilisation ultérieure.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidéo numérique dans DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Données DV au format de fichier AVI](dv-data-in-the-avi-file-format.md)
</dt> <dt>

[Pilote MSDV](msdv-driver.md)
</dt> </dl>

 

 



