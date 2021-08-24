---
description: Exemple DVApp
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: Exemple DVApp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72067c04e108354c1706690bc71e8b339ad5af071c46cc0e4102ae10e9a3643f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148722"
---
# <a name="dvapp-sample"></a>Exemple DVApp

## <a name="description"></a>Description

Application de capture vidéo numérique (DV).

Cet exemple montre comment créer différents types de graphiques de filtre pour contrôler les caméscopes DV. Il montre également comment effectuer des captures, des aperçus, des transmissions et des contrôles d’appareil avec un caméscope DV.

### <a name="usage"></a>Usage

L’application DVApp prend en charge les modes suivants :

-   Aperçu : effectue le rendu du DV à partir du caméscope dans une fenêtre vidéo.
-   Fichier DV vers type-1 : capture les données DV du caméscope dans un fichier DV de type 1.
-   Tapez-1 fichier sur DV : transmet les données d’un fichier DV type-1 au caméscope.
-   Fichier DV vers type-2 : capture les données DV du caméscope dans un fichier DV de type 2.
-   Tapez-2 fichier sur DV : transmet les données d’un fichier DV type-2 au caméscope.

Les modes capture et transmission effectuent également une préversion. Chacun de ces modes n’a **pas** d’option d’aperçu, ce qui désactive la version préliminaire. La capture sans aperçu est plus efficace et peut réduire le nombre d’images supprimées.

L’application démarre en mode aperçu. pour sélectionner un autre mode, choisissez un mode dans le menu **Graph mode** . Pour chaque mode, DVApp génère un graphique de filtre qui prend en charge les fonctionnalités de ce mode. pour enregistrer le graphique en tant que fichier GraphEdit (. grf), sélectionnez **enregistrer Graph dans un fichier** dans le menu **fichier** . Quittez DVApp avant d’ouvrir le fichier dans GraphEdit.

Pour capturer dans un fichier :

1.  Dans le menu **fichier** , choisissez **définir le fichier de sortie** et entrez un nom de fichier.
2.  dans le menu **Graph mode** , sélectionnez un mode *DV vers fichier* (tapez 1 ou tapez 2, avec ou sans aperçu).
3.  Cliquez sur **Enregistrer**.
4.  Si le caméscope est en mode VTR, cliquez sur **lire**.
5.  Pour arrêter la capture, cliquez sur **arrêter**.

Pour transmettre un fichier au caméscope, procédez comme suit :

1.  Dans le menu **fichier** , cliquez sur **définir le fichier d’entrée** et sélectionnez un fichier DV. Le fichier doit correspondre au mode sélectionné (type 1 ou type 2).
2.  dans le menu du **mode Graph** , sélectionnez un fichier en mode *DV* (tapez 1 ou tapez 2, avec ou sans aperçu).
3.  Cliquez sur **Lire**.
4.  Pour enregistrer les données sur bande, cliquez sur **Enregistrer**.
5.  Pour arrêter la transmission, cliquez sur **arrêter**.

Si le caméscope est en mode VTR, l’utilisateur peut contrôler le mécanisme de transport via les boutons de style VCR de l’application. Pour rechercher la bande, entrez le code temporel cible, puis cliquez sur le bouton Rechercher.

Pour limiter la quantité de données capturées par l’application, choisissez **taille de capture** dans le menu **fichier** .

Pour vérifier le format de bande (NTSC ou PAL), choisissez **Vérifier la bande** dans le menu **options** .

Pour modifier la taille de la fenêtre d’aperçu, choisissez **modifier la taille du décodage** dans le menu **options** .

### <a name="programming-notes"></a>Notes de programmation

L’objectif principal de cette application est de montrer comment créer différents graphiques de capture DV et de transmission.

### <a name="device-arrival-and-removal"></a>Arrivée et suppression de l’appareil

L’application gère l’arrivée et la suppression des appareils à l’aide de deux techniques différentes. Pour l’arrivée de l’appareil, la boucle de message de l’application répond aux \_ messages WM DEVICECHANGE. Pour la suppression de l’appareil, l’application répond aux événements de [**\_ \_ perte d’appareil EC**](ec-device-lost.md) du gestionnaire de graphes de filtre. L’une ou l’autre approche fonctionne, bien que l' \_ \_ événement de perte de l’appareil EC dépende de l’existence de l’appareil dans le graphique de filtre.

L’application ne gère qu’un seul appareil à la fois. Si l’appareil en cours est supprimé, l’application recherche un autre périphérique DV sur le système.

Sur certains caméscopes DV, l’utilisateur doit éteindre l’appareil lors de son basculement entre le mode caméra et le mode VTR, ce qui déclenche un message de perte d’appareil. L’application répond en activant ou désactivant les commandes de menu appropriées. Toutefois, si l’utilisateur bascule rapidement entre les modes, il se peut que le caméscope ne génère pas de message de perte d’appareil. Vous pouvez forcer la mise à jour des menus en choisissant le **mode d’actualisation** dans le menu **options** . Certains caméscopes DV peuvent basculer les modes sans éteindre l’appareil, mais envoyer un message perdu uniquement quand ils basculent en mode VTR.

### <a name="device-control"></a>Contrôle de l’appareil

La fonctionnalité du bouton **lire** et **Enregistrer** dépend du mode actuel :

-   Aperçu : le graphique de filtre s’exécute automatiquement. Le bouton de **lecture** démarre le transport.
-   Capturer dans un fichier : le bouton d' **enregistrement** exécute le graphique et le bouton de **lecture** démarre le transport.
-   Transmettre à l’appareil : le bouton de **lecture** exécute le graphique et le bouton d' **enregistrement** démarre le transport.

L’exemple d’application n’effectue pas de capture de précision de trame. À différents moments, l’application appelle la fonction **Sleep** pour attendre que l’appareil réponde. Les nouveaux caméscopes DV envoient une notification lorsque l’état de l’appareil change. Les appareils plus anciens peuvent ne pas prendre en charge la notification. dans le cadre d’un exemple, l’appel de **Sleep** est une solution plus simple.

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] du kit de développement logiciel (SDK)* \\ \\ \\ DirectShow \\ capturer les \\ DVApp.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle d’un caméscope DV](controlling-a-dv-camcorder.md)
</dt> <dt>

[Vidéo numérique en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[DirectShow Extraits](directshow-samples.md)
</dt> </dl>

 

 



