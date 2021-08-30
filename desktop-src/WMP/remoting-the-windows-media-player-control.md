---
title: Utilisation à distance du contrôle Windows Media Player
description: Utilisation à distance du contrôle Windows Media Player
ms.assetid: d543b2a0-a2cb-47e2-b50e-4513fc061b46
keywords:
- Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet, incorporation ActiveX contrôle
- Lecteur Windows Media Mobile, incorporation ActiveX contrôle
- contrôle de ActiveX Lecteur Windows Media, incorporation
- Lecteur Windows Media contrôle de ActiveX Mobile, incorporation
- contrôle de ActiveX, incorporation
- Lecteur Windows Media, contrôle de ActiveX à distance
- modèle objet Lecteur Windows Media, contrôle de ActiveX à distance
- modèle objet, communication à distance ActiveX contrôle
- Lecteur Windows Media contrôle de ActiveX Mobile, remoting
- contrôle de ActiveX Lecteur Windows Media, communication à distance
- Lecteur Windows Media contrôle de ActiveX Mobile, communication à distance
- contrôle de ActiveX, communication à distance
- contrôle de ActiveX Lecteur Windows Media de communication à distance
- incorporation, communication à distance ActiveX contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5d067fdc0846c1d7ccfcd828d55adbb5b5e74c52f9bb5f468d86192655004c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002609"
---
# <a name="remoting-the-windows-media-player-control"></a>Utilisation à distance du contrôle Windows Media Player

lorsque vous incorporez le contrôle Lecteur Windows Media dans un programme C++, vous pouvez l’utiliser en tant qu’extension distante du mode complet du lecteur. c’est ce que l’on appelle la « communication à distance » du contrôle Lecteur Windows Media, et vous permet de fournir toutes les fonctionnalités du lecteur en mode complet sans les implémenter vous-même.

Lorsque vous disposez d’un contrôle à distance, il partage le même moteur de lecture que le mode complet du lecteur et vos utilisateurs peuvent basculer entre le mode incorporé (l’état « ancré ») et le mode plein (l’état « non ancré »), tandis que la lecture des médias numériques se poursuit sans interruption.

## <a name="enabling-remote-embedding"></a>Activation de l’incorporation à distance

pour permettre l’incorporation à distance du contrôle Lecteur Windows Media, votre programme doit implémenter les interfaces **IServiceProvider** et [IWMPRemoteMediaServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices) . **IServiceProvider** est une interface com (Component Object Model) standard avec une méthode unique appelée **QueryService**. Lecteur Windows Media appelle cette méthode pour récupérer un pointeur vers une interface **IWMPRemoteMediaServices** .

**IWMPRemoteMediaServices** a plusieurs méthodes, mais seules deux d’entre elles sont directement pertinentes pour la communication à distance. dans [GetApplicationName](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getapplicationname), vous retournez le nom de votre programme, que Lecteur Windows Media ajoute à la liste **basculer vers un autre programme** du menu **affichage** . Dans [GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype), vous indiquez le mode d’incorporation du contrôle en retournant une valeur « Remote » ou « local ». Si une connexion à distance est établie, la méthode [obtenir \_ isRemote](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_isremote) de l’interface [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4) retourne la valeur true.

## <a name="specifying-an-exclusive-online-store"></a>Spécification d’un magasin en ligne exclusif

avec Lecteur Windows Media 11, une application qui incorpore le contrôle du lecteur à distance peut spécifier un magasin en ligne exclusif. dans ce cas, le sélecteur de service dans Lecteur Windows Media est désactivé et seule la banque en ligne spécifiée est disponible pour l’utilisateur. Pour plus d’informations sur la façon de spécifier un magasin en ligne exclusif, consultez [magasins en ligne exclusifs](exclusive-online-stores.md).

## <a name="docking-and-undocking"></a>Ancrage et déconnexion

L’interface **IWMPPlayer4** fournit également l’accès à l’interface [IWMPPlayerApplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication) par le biais de la méthode [ \_ playerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_playerapplication) . Utilisez **IWMPPlayerApplication** pour basculer entre les États ancré et non ancré et pour déterminer l’état ancré actuel et l’emplacement de l’affichage vidéo ou visualisation.

la méthode [IWMPPlayerApplication :: switchToPlayerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtoplayerapplication) détache le contrôle en ouvrant le mode complet de Lecteur Windows Media et en transférant l’affichage de la vidéo ou de la visualisation vers le volet **playing Now** . La méthode [IWMPPlayerApplication :: switchToControl](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtocontrol) ancre le contrôle en transférant l’affichage de la vidéo ou de la visualisation à votre programme et en fermant le mode complet du joueur, s’il est ouvert. Le contrôle peut également être ancré en sélectionnant un programme dans la liste **basculer vers un autre programme** ou en fermant le mode complet du lecteur. Dans les deux cas, tous les supports numériques en cours de diffusion se poursuivent sans interruption.

## <a name="transferring-the-video-or-visualization-display"></a>Transfert de l’affichage de la vidéo ou de la visualisation

lorsque plusieurs programmes avec des contrôles Lecteur Windows Media distants incorporés s’exécutent simultanément, tous les contrôles partagent le même moteur de lecture. Ils partagent également la même instance du mode complet du lecteur dans un État non ancré. Dans l’État ancrée, toutefois, un seul contrôle peut afficher la vidéo ou la visualisation. Dans l’état non ancré, seul le mode complet du lecteur affiche la vidéo ou la visualisation. La méthode **switchToControl** fonctionne à la fois dans les États ancrés et non ancrés et transfère l’affichage de la vidéo ou de la visualisation vers le programme qui l’appelle.

la seule différence entre les états ancré et non ancré est la présence du mode complet de Lecteur Windows Media et sa propriété de l’affichage vidéo ou visualisation. Dans l’état non ancré, tous les contrôles incorporés à distance en cours d’exécution sont toujours visibles et leurs interfaces utilisateur sont toujours entièrement fonctionnelles. Toutefois, si une fenêtre vidéo ou de visualisation est présente, elle est vide. Dans l’état ancré, seul l’un des contrôles incorporés et distants est propriétaire de l’affichage, mais toutes les interfaces utilisateur continuent à fonctionner.

## <a name="hiding-or-changing-the-control-in-the-undocked-state"></a>Masquage ou modification du contrôle dans l’état non ancré

Vous devez fournir votre propre implémentation si vous souhaitez masquer ou modifier l’interface utilisateur d’un contrôle incorporé dans un État non ancré ou lorsque votre programme n’est pas propriétaire de l’affichage. vous pouvez apporter ces modifications lorsque vous ancrez et détachez le contrôle, ou vous pouvez les créer en réponse à des événements de Lecteur Windows Media. Étant donné que le joueur peut être ancré par le biais de l’option **de menu basculer vers un autre programme** , il est généralement préférable de fournir cette fonctionnalité en réponse aux événements.

Vous pouvez implémenter des gestionnaires d’événements pour les événements [SwitchedToPlayerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication) et [SwitchedToControl](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol) , ou vous pouvez implémenter un gestionnaire d’événements unique pour l’événement [PlayerDockedStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange) . Dans ce dernier cas, vous pouvez déterminer l’état ancré en appelant [IWMPPlayerApplication :: obtenir \_ playerDocked](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_playerdocked). Dans les deux cas, utilisez [IWMPPlayerApplication :: obtenir \_ hasDisplay](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_hasdisplay) pour déterminer si votre programme est propriétaire de l’affichage vidéo ou visualisation.

## <a name="re-establishing-a-remote-connection"></a>Réinitialisation d’une connexion à distance

dans certains cas, la connexion entre un contrôle incorporé à distance et le lecteur autonome échoue, invalidant les pointeurs vers les interfaces Lecteur Windows Media. Lecteur Windows Media tentera automatiquement de se reconnecter et déclenchera l’événement [PlayerReconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect) pour signaler cette tentative. Bien que la reconnexion soit automatique, vous devez fournir un gestionnaire d’événements pour cet événement si vous souhaitez libérer vos pointeurs non valides et en récupérer de nouveaux afin de pouvoir accéder au lecteur autonome via la nouvelle connexion.

## <a name="controlling-the-undocked-player"></a>Contrôle du joueur non ancré

toutes les instances distantes du contrôle Lecteur Windows Media peuvent manipuler le mode complet du lecteur, quel que soit l’état d’ancrage. toutefois, les fonctionnalités qui n’ont aucune pertinence pour le mode complet du lecteur sont ignorées jusqu’à ce que le contrôle Lecteur Windows Media soit ancré. Cela comprend les propriétés des [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) et des interfaces dérivées, telles que **Enabled**, **enableContextMenu**, **UIMODE** et **windowlessVideo**.

## <a name="error-dialog-boxes"></a>Boîtes de dialogue d’erreur

à partir d’une instance de contrôle de Lecteur Windows Media distante, le *Paramètres*. la propriété **enableErrorDialogs** se comporte de manière spécifique. Les règles suivantes s’appliquent :

-   lorsque Lecteur Windows Media est déconnectée (l’interface utilisateur Lecteur Windows Media est visible), la propriété **enableErrorDialogs** est ignorée et les boîtes de dialogue d’erreur sont gérées par le lecteur.
-   lorsque Lecteur Windows Media est ancrée, la valeur spécifiée par chaque instance distante du contrôle pour **enableErrorDialogs** s’applique uniquement à l’instance de contrôle individuelle. Autrement dit, si une instance de contrôle particulière spécifie la valeur « true » pour **enableErrorDialogs**, seule cette instance affiche une boîte de dialogue quand une erreur se produit si toutes les autres instances du contrôle ont spécifié la valeur « false ».

## <a name="remoting-in-the-background"></a>Communication à distance en arrière-plan

Évitez de conserver une instance distante du lecteur en cours d’exécution en arrière-plan pendant les périodes où le contrôle n’est pas utilisé. Étant donné que l’instance de contrôle de lecteur distant partage son moteur de lecture avec le lecteur en mode complet, le fait de maintenir une instance d’arrière-plan en cours d’exécution peut entraîner un comportement inattendu. Par exemple, l’utilisateur peut fermer le lecteur en mode complet pendant la lecture d’un fichier. L’utilisateur s’attend à ce que la lecture du fichier s’arrête complètement lorsque le joueur se ferme, mais le son peut continuer à fonctionner car le moteur de lecture est toujours actif.

## <a name="samples"></a>Exemples

le package d’installation du kit de développement logiciel Lecteur Windows Media installe des exemples qui illustrent la communication à distance. Pour plus d’informations, consultez les exemples RemoteSkin et WMPML.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemples**](samples.md)
</dt> <dt>

[**utilisation du contrôle Lecteur Windows Media dans un programme C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




