---
description: La correction gamma, ou gamma pour Short, est le nom d’une opération non linéaire que les systèmes utilisent pour coder et décoder les valeurs de pixel dans les images.
ms.assetid: 97ACDAE3-514E-4AAF-A27D-E5FFC162DB2A
title: Utilisation de la correction gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c5f5d3af8550f86280e6203858444469a5aa8caaab462f560da152caaa2a76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118288962"
---
# <a name="using-gamma-correction"></a>Utilisation de la correction gamma

La correction gamma, ou gamma pour Short, est le nom d’une opération non linéaire que les systèmes utilisent pour coder et décoder les valeurs de pixel dans les images.

-   [Qu’est-ce que le gamma et à quoi sert-il ?](#what-is-gamma-and-what-is-it-for)
-   [Arrière-plan de gamma sur Windows](#background-of-gamma-on-windows)
-   [Évolution de l’affichage du matériel](#evolution-of-display-hardware)
-   [Fonctionnalités de contrôle gamma dans DXGI](#gamma-control-capabilities-in-dxgi)
-   [Définition du contrôle gamma avec DXGI](#setting-gamma-control-with-dxgi)
-   [Pratiques de contrôle gamma](#gamma-control-practicalities)
-   [Rubriques connexes](#related-topics)

## <a name="what-is-gamma-and-what-is-it-for"></a>Qu’est-ce que le gamma et à quoi sert-il ?

À la fin du pipeline graphique, juste où l’image laisse l’ordinateur effectuer son parcours le long du câble du moniteur, il y a un petit morceau de matériel capable de transformer les valeurs de pixel à la volée. Ce matériel utilise généralement une table de recherche pour transformer les pixels. Ce matériel utilise les valeurs rouge, vert et bleu qui proviennent de la surface à afficher pour rechercher les valeurs corrigées gamma dans la table, puis envoie les valeurs corrigées à l’analyse à la place des valeurs de surface réelles. Par conséquent, cette table de recherche est une opportunité de remplacer toute couleur par une autre couleur. Bien que la table ait ce niveau de puissance, l’utilisation classique consiste à ajuster les images de façon subtile pour compenser les différences dans la réponse du moniteur. La réponse du moniteur est la fonction qui lie la valeur numérique des composants rouge, vert et bleu d’un pixel avec la luminosité affichée de ce pixel.

C’est ce que ce tableau était destiné, mais les développeurs de jeux ont trouvé des utilisations créatives, telles que le clignotement de l’écran entier en rouge pour l’effet psychologique. Dans les applications de jeu modernes, dans le cadre du traitement de chaque trame, nous fournissons généralement d’autres façons d’effectuer ces opérations. En fait, nous vous recommandons de conserver la table gamma seule, car elle peut être utilisée pour étalonner la réponse du moniteur, et les modifications de gros à la rampe gamma entraîneront la destruction de cet étalonnage minutieux.

La science de la détermination de la correction gamma est complexe et n’est pas présentée ici, sauf pour éclairer l’origine du nom « gamma ». La réponse d’un moniteur CRT (autrement dit, une plus ancienne vitre) est une fonction complexe, mais la physique de ces analyses signifie qu’elles présentent une réponse qui peut être représentée de manière brute par cette fonction d’alimentation :

luminosité (entrée) =<sup>gamma</sup> d’entrée

La valeur gamma est généralement proche de la valeur 2,0. Les moniteurs LCD et toutes les autres technologies plus récentes sont spécialement conçus pour présenter une réponse similaire, de sorte que l’ensemble de nos logiciels et images n’ont pas besoin d’être recalibrés pour ces nouvelles technologies. La norme sRVB déclare que cette valeur gamma est exactement 2,2, et cette valeur est devenue une norme largement implémentée.

L’œil humain possède également une fonction de réponse qui inverse approximativement la fonction d’alimentation du CRT. Cela signifie que la luminosité perçue d’un pixel augmente à peu près de manière linéaire avec les valeurs RVB dans ce pixel.

Étant donné qu’une valeur gamma de 2,2 est devenue une norme de facto, nous n’avons généralement pas besoin de se soucier trop de la courbe gamma encodée dans cette table et peuvent la conserver sous la forme d’un mappage de type un-à-un linéaire. La correspondance des couleurs appropriée fait évidemment appel à cette fonction, mais cette discussion n’entre pas dans le cadre de cette rubrique. Windows comprend un outil qui permet aux utilisateurs d’étalonner leur affichage à la valeur gamma 2,2, et cet outil utilise le matériel de table de recherche pour dériver une modification subtile soigneusement choisie pour leurs ordinateurs. Les utilisateurs peuvent exécuter cet outil en recherchant « CALIBRATE Color ». Il existe également des profils de couleurs bien définis pour des analyses spécifiques qui automatisent ce processus. L’outil « calibrage des couleurs » peut détecter ces moniteurs plus récents et informer les utilisateurs que l’étalonnage est déjà en place.

Cette notion d’encodage d’une loi d’alimentation en valeurs de couleur est utile ailleurs dans le pipeline graphique, en particulier dans les textures. Pour les textures, vous souhaitez une plus grande précision sur les couleurs plus foncées en raison de la réponse logarithmique de l’oeil humain que nous venons de parler. Une gestion attentive de gamma dans cette partie du pipeline est importante. Pour plus d’informations, consultez [conversion de données pour l’espace colorimétrique](converting-data-color-space.md).

Le reste de cette rubrique se concentre uniquement sur la correction gamma dans cette dernière partie du pipeline, entre les données de la mémoire tampon de trame et l’analyse. Si vous souhaitez écrire un assistant d’étalonnage ou créer des effets spéciaux dans une application en plein écran où une étape de traitement n’est pas pratique, Voici les informations dont vous avez besoin.

## <a name="background-of-gamma-on-windows"></a>Arrière-plan de gamma sur Windows

Windows ordinateurs possèdent généralement une table gamma qui est une table de recherche qui accepte un triple d’octets et génère un triple d’octets. Ces triplets sont 768 (256 x 3) octets de RAM. C’est parfait lorsque votre format d’affichage contient un triple de valeurs d’octets RVB, mais n’est pas suffisamment expressif pour décrire les transformations que vous pouvez souhaiter lorsque le format d’affichage a une plage supérieure à \[ 0, \] par exemple les valeurs à virgule flottante. les api de Windows qui contrôlent le gamma ont suivi une évolution dans la mesure où les formats d’affichage sont devenus plus complexes.

la première Windows api pour offrir le contrôle gamma est Windows le [**SetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp) et le [**GetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-getdevicegammaramp)Graphics Device Interface (GDI). Ces API fonctionnent avec des tableaux de mots de 3 256 entrées, chaque mot encodant zéro, représenté par les valeurs de mot 0 et 65535. La précision supplémentaire d’un mot n’est généralement pas disponible dans les tables de recherche de matériel réelles, mais ces API ont été conçues pour être flexibles. Ces API, contrairement aux autres décrites plus loin dans cette section, n’autorisent qu’un petit écart par rapport à une fonction d’identité. En fait, toute entrée de la rampe doit être comprise entre 32768 et la valeur d’identité. Cette restriction signifie qu’aucune application ne peut activer l’affichage entièrement noir ou une autre couleur illisible.

L’API suivante est [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)de Microsoft Direct3D 9, qui suit les mêmes modèle et format de données que [**SetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp). La valeur par défaut de la rampe gamma Direct3D 9 n’est pas particulièrement utile. Il s’agit d’une rampe de mots initialisée à 0-255, et non à 0-65535, même si l’API est définie en termes de 0-65535.

La dernière API est [**IDXGIOutput :: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol). Cette API a un schéma plus flexible pour exprimer le contrôle gamma, tout comme l’ensemble de formats d’affichage DXGI, y compris dix bits par canal, les formats float de 16 bits et le format de \_ plage étendue XR Bias.

Toutes ces API fonctionnent sur le même matériel et modifient les mêmes valeurs. Les API Direct3D 9 et DXGI sont en « écriture seule ». Vous ne pouvez pas lire la valeur du matériel, la modifier, puis la définir. Vous pouvez uniquement définir la rampe. En outre, vous pouvez uniquement définir la valeur gamma lorsque l’application est en mode plein écran. Cette restriction est un autre moyen de garantir que le bureau est toujours lisible. autrement dit, l’application peut perturber son propre affichage, mais Windows restaurera la rampe gamma précédente lorsque l’application perdra en mode plein écran (par exemple, via alt-tab ou ctrl-alt-del).

## <a name="evolution-of-display-hardware"></a>Évolution de l’affichage du matériel

Certaines analyses plus récentes peuvent afficher une large gamme d’intensités. Toutefois, lorsque le format d’affichage peut représenter uniquement des valeurs comprises entre zéro et un, l’affichage doit mapper zéro à sa valeur la plus foncée et l’autre à sa valeur la plus claire. Cette valeur la plus brillante peut être trop brillante pour une vue confortable des pages Web avec du texte noir sur un arrière-plan blanc, mais très belle pour des effets spéciaux trop brillants, tels que la visualisation de la lumière du soleil Glittering sur un lac ou une foudre fourche du ciel. Nous avons donc besoin d’un moyen d’exprimer ces plages plus larges. DXGI 1,1 et ultérieur contient des valeurs de format d’affichage qui permettent à 1,0 de représenter une valeur blanche familière et réserve des valeurs de format d’affichage plus larges pour des effets spéciaux surbrillants. DXGI 1,1 prend en charge deux formats d’affichage qui peuvent exprimer ces valeurs plus larges : DXGI \_ format \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM et 16 bits à virgule flottante. Pour une description complète de ces formats, consultez [Détails du format étendu](/windows-hardware/drivers/display/details-of-the-extended-format). Ensuite, nous examinons la raison pour laquelle l’API gamma [**IDXGIOutput :: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) de dxgi a besoin de valeurs en pixels supérieures à 1,0.

## <a name="gamma-control-capabilities-in-dxgi"></a>Fonctionnalités de contrôle gamma dans DXGI

DXGI permet au pilote d’affichage d’exprimer ses contrôles gamma comme une fonction linéaire à l’étape. Cette fonction linéaire à l’étape est définie par les points de contrôle de cette fonction, la plage de valeurs vers laquelle la fonction peut effectuer la conversion, et une opération supplémentaire de mise à l’échelle et de décalage qui peut être appliquée après la conversion. Une application peut appeler la méthode [**IDXGIOutput :: GetGammaControlCapabilities**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) pour récupérer toutes ces fonctionnalités de contrôle dans la structure de [**\_ \_ \_ fonctionnalités de contrôle gamma dxgi**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) .

Ce graphique illustre une fonction linéaire avec seulement quatre points de contrôle.

![fonction linéaire de correction gamma](images/gamma-linear-function.png)

DXGI définit les points de contrôle par leur emplacement le long de l’axe des couleurs de surface. Dans le graphique précédent, les emplacements des points de contrôle sont 0, 0,5, 0,75 et 1,0. Ces points de contrôle indiquent que le matériel peut convertir les valeurs de la plage 0 à 1,0. DXGI répertorie ces points de contrôle dans le membre de tableau **ControlPointPositions** des [**\_ \_ \_ fonctionnalités de contrôle gamma dxgi**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) et les déclare toujours dans l’ordre de croissance. DXGI remplit uniquement les premiers éléments du tableau **ControlPointPositions** et indique le nombre d’éléments avec le membre **NumGammaControlPoints** des fonctionnalités de **\_ \_ contrôle \_ gamma dxgi**. Si **NumGammaControlPoints** est inférieur à 1025, DXGI laisse les autres éléments **ControlPointPositions** non définis.

Le matériel représenté par ce graphique peut convertir les valeurs dans une plage comprise entre 0 et 1,25. Par conséquent, DXGI définit les membres **MinConvertedValue** et **MaxConvertedValue** sur 0.0 f et 1,25 f respectivement.

DXGI définit le membre **ScaleAndOffsetSupported** des [**\_ \_ \_ fonctionnalités de contrôle gamma dxgi**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) pour indiquer si le matériel prend en charge la fonctionnalité de mise à l’échelle et de décalage. Si le matériel prend en charge la mise à l’échelle et le décalage, il conserve une table de recherche un-à-un simple, mais ajuste la sortie de la table pour étirer la sortie vers une plage supérieure à \[ 0, 1 \] . Le matériel met d’abord à l’échelle les valeurs provenant de la table de recherche, puis les décale.

> [!Note]  
> Différentes analyses peuvent être connectées à un même ordinateur. En outre, les capacités de contrôle gamma peuvent en effet changer en fonction du mode d’affichage de la sortie. Par conséquent, nous vous recommandons de toujours appeler [**IDXGIOutput :: GetGammaControlCapabilities**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) pour interroger les fonctionnalités de contrôle gamma une fois que votre application passe en mode plein écran.

 

Vous pouvez utiliser ces valeurs de capacité de contrôle gamma pour dériver des valeurs de contrôle que vous pouvez ensuite définir à l’aide de l’API [**IDXGIOutput :: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) .

## <a name="setting-gamma-control-with-dxgi"></a>Définition du contrôle gamma avec DXGI

Pour définir des contrôles gamma, vous transmettez un pointeur vers une structure de [**\_ \_ contrôle gamma dxgi**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) quand vous appelez l’API [**IDXGIOutput :: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) .

Vous définissez les membres **Scale** et **offset** du [**\_ \_ contrôle gamma dxgi**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) pour spécifier les valeurs de mise à l’échelle et de décalage que vous souhaitez que le matériel applique aux valeurs que vous recevez de la table de recherche. Vous pouvez définir en toute sécurité la mise à l' **échelle** sur 1 et le **décalage** à zéro (autrement dit, une échelle d’une unité n’a aucun effet et un décalage de zéro n’a aucun effet) si vous ne souhaitez pas utiliser la fonction de mise à l’échelle et de décalage ou si le matériel n’a pas cette fonctionnalité.

Vous définissez le  membre de tableau GammaCurve [**du \_ \_ contrôle gamma dxgi**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) sur une liste de structures [**\_ RGB dxgi**](/previous-versions/windows/desktop/legacy/bb173071(v=vs.85)) pour les points sur la courbe gamma. Chaque **élément \_ RGB dxgi** spécifie les valeurs float qui représentent les composants rouge, vert et bleu pour ce point. La courbe gamma n’utilise pas de valeurs alpha. Vous utilisez le nombre que vous avez obtenu à partir de **NumGammaControlPoints** de [**\_ \_ \_ fonctionnalités de contrôle gamma dxgi**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) pour remplir ce nombre d’éléments dans le tableau **GammaCurve** . Chaque élément que vous placez dans le tableau **GammaCurve** correspond à la hauteur de chaque point de contrôle.

Notez dans le graphique précédent que vous contrôlez maintenant le positionnement vertical de chaque point de contrôle et que vous disposez d’un contrôle distinct pour le rouge, le vert et le bleu. Par exemple, vous pouvez définir toutes les valeurs vert et bleu sur zéro et définir les valeurs rouges sur un escalier croissant de zéro à 1. Dans ce scénario, l’image affichée affiche uniquement ses parties rouges, le bleu et le vert apparaissant en noir. Vous pouvez également définir un escalier décroissant pour toutes les couleurs, ce qui entraîne un affichage inversé. Toute valeur que vous placez dans le tableau **GammaCurve** doit être comprise dans les valeurs que vous avez obtenues à partir des membres **MinConvertedValue** et **MaxConvertedValue** des [**\_ \_ \_ fonctionnalités de contrôle gamma dxgi**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)).

## <a name="gamma-control-practicalities"></a>Pratiques de contrôle gamma

Les contrôles gamma de DXGI s’appliquent uniquement tant que l’application est en mode plein écran. Windows restaure l’état précédent de l’affichage lorsque l’application s’arrête ou retourne en mode fenêtre. mais Windows ne restaure pas l’état gamma de votre application si l’application entre en mode plein écran. Votre application doit restaurer explicitement son état gamma lorsqu’elle revient en mode plein écran.

Tous les adaptateurs ne prennent pas en charge le contrôle gamma. Si un adaptateur ne prend pas en charge le contrôle gamma, il ignore les appels pour définir une rampe gamma.

Les applications qui s’exécutent sous le Bureau à distance ne peuvent pas contrôler le gamma du tout.

Le curseur de la souris, s’il est implémenté dans le matériel (le plus souvent), ne répond généralement pas au paramètre gamma.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
