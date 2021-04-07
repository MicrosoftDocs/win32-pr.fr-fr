---
description: Cette rubrique explique comment écrire un convertisseur vidéo personnalisé pour DirectShow.
ms.assetid: abba5113-125f-4dac-b566-99c0d9b5978c
title: Autres convertisseurs vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070e55375d9d1d5a32c306853aafcb431a76c368
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747277"
---
# <a name="alternative-video-renderers"></a>Autres convertisseurs vidéo

Cette rubrique explique comment écrire un convertisseur vidéo personnalisé pour DirectShow.

> [!Note]  
> Au lieu d’écrire un convertisseur vidéo personnalisé, il est recommandé d’écrire un allocateur de plug-in pour le convertisseur de mixage vidéo (VMR) ou le [**convertisseur vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR). Cette approche vous offre tous les avantages de VMR/EVR, y compris la prise en charge de DirectX Video Acceleration (DXVA), le désentrelacement matériel et le pas à pas, et est susceptible d’être plus robuste qu’un convertisseur vidéo personnalisé. Pour plus d'informations, voir les rubriques suivantes :
>
> -   [Mode de lecture non rendu VMR (Allocator personnalisé-présentateur)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
> -   [Comment écrire un présentateur EVR](/windows/desktop/medfound/how-to-write-an-evr-presenter)

 

## <a name="writing-an-alternative-renderer"></a>Écriture d’un convertisseur de remplacement

Microsoft DirectShow fournit un convertisseur vidéo basé sur une fenêtre ; Il fournit également un convertisseur plein écran dans l’installation. Vous pouvez utiliser les classes de base DirectShow pour écrire d’autres convertisseurs vidéo. Pour que d’autres convertisseurs interagissent correctement avec les applications DirectShow, les convertisseurs doivent respecter les instructions décrites dans cet article. Vous pouvez utiliser les classes [**CBaseRenderer**](cbaserenderer.md) et [**CBaseVideoRenderer**](cbasevideorenderer.md) pour suivre ces instructions lors de l’implémentation d’un rendu de vidéo alternatif. En raison du développement en cours de DirectShow, examinez régulièrement votre implémentation pour vous assurer que les convertisseurs sont compatibles avec la version la plus récente de DirectShow.

Cette rubrique traite de nombreuses notifications qu’un convertisseur est responsable de la gestion. Un bref aperçu des notifications DirectShow peut vous aider à définir la phase. Il existe essentiellement trois types de notifications qui se produisent dans DirectShow :

-   Les *notifications de flux*, qui sont des événements qui se produisent dans le flux de média et sont passées d’un filtre à l’autre. Il peut s’agir de début, de vidage ou de notifications de fin de flux et sont envoyés en appelant la méthode appropriée sur la broche d’entrée du filtre en aval (par exemple [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)).
-   *Filtrez les notifications de graphique*, qui sont des événements envoyés à partir d’un filtre au gestionnaire de graphique de filtre, par exemple [**EC \_ Complete**](ec-complete.md). Pour ce faire, vous devez appeler la méthode [**IMediaEventSink :: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) sur le gestionnaire de graphique de filtre.
-   Les *notifications d’application*, qui sont récupérées à partir du gestionnaire de graphique de filtre par l’application de contrôle. Une application appelle la méthode [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) sur le gestionnaire de graphique de filtre pour récupérer ces événements. Souvent, le gestionnaire de graphique de filtre traverse les événements qu’il reçoit à l’application.

Cette rubrique décrit la responsabilité du filtre de convertisseur dans la gestion des notifications de flux qu’il reçoit et dans l’envoi de notifications de graphique de filtre appropriées.

## <a name="handling-end-of-stream-and-flushing-notifications"></a>Gestion des notifications de fin de flux et de vidage

Une notification de fin de flux commence au niveau d’un filtre amont (tel que le filtre source) lorsque ce filtre détecte qu’il ne peut pas envoyer plus de données. Elle est passée par chaque filtre dans le graphique et finit par se terminer au niveau du convertisseur, qui est responsable de l’envoi par la suite d’une notification d' [**\_ achèvement ce**](ec-complete.md) au gestionnaire de graphes de filtres. Les convertisseurs ont des responsabilités spéciales lorsqu’il s’agit de gérer ces notifications.

Un convertisseur reçoit une notification de fin de flux lorsque la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) de son pin d’entrée est appelée par le filtre amont. Un convertisseur doit noter cette notification et continuer à afficher toutes les données qu’il a déjà reçues. Une fois que toutes les données restantes ont été reçues, le convertisseur doit envoyer une notification d' [**\_ achèvement ce**](ec-complete.md) au gestionnaire de graphes de filtre. La notification d' **\_ achèvement ce** ne doit être envoyée qu’une seule fois par un convertisseur à chaque fois qu’elle atteint la fin d’un flux. En outre, les notifications d' **\_ achèvement ce** ne doivent jamais être envoyées, sauf lorsque le graphique de filtre est en cours d’exécution. Par conséquent, si le graphique de filtre est suspendu lorsqu’un filtre source envoie une notification de fin de flux, **ce dernier \_** ne doit pas être envoyé tant que le graphique de filtre n’est pas exécuté.

Tous les appels aux méthodes [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) ou [**IMemInputPin :: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) après une notification de fin de flux signalée doivent être rejetés. **E \_ INATTENDU** est le message d’erreur le plus approprié à retourner dans ce cas.

Lorsqu’un graphique de filtre est arrêté, toutes les notifications de fin de flux mises en cache doivent être effacées et ne pas être renvoyées au prochain démarrage. Cela est dû au fait que le gestionnaire de graphique de filtre suspend toujours tous les filtres juste avant de les exécuter afin que le vidage correct se produise. Ainsi, par exemple, si le graphique de filtre est suspendu et qu’une notification de fin de flux est reçue, puis que le graphique de filtre est arrêté, le convertisseur ne doit pas envoyer de notification d' [**\_ achèvement ce**](ec-complete.md) lorsqu’il est exécuté par la suite. Si aucune recherche n’a eu lieu, le filtre source envoie automatiquement une autre notification de fin de flux lors de l’état de pause qui précède un état d’exécution. Si, en revanche, une recherche s’est produite alors que le graphique de filtre est arrêté, le filtre source peut contenir des données à envoyer, de sorte qu’il n’envoie pas de notification de fin de flux.

Les convertisseurs vidéo dépendent souvent des notifications de fin de flux pour plus que l’envoi des notifications [**\_ complètes EC**](ec-complete.md) . Par exemple, si un flux a fini de s’exécuter (autrement dit, une notification de fin de flux est envoyée) et qu’une autre fenêtre est glissée sur une fenêtre de convertisseur vidéo, un certain nombre de messages de fenêtre de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) seront générés. La pratique courante pour l’exécution de convertisseurs vidéo consiste à ne pas redessiner le frame en cours lors de la réception des messages de **\_ peinture WM** (en partant de l’hypothèse qu’une autre image à dessiner sera reçue). Toutefois, lorsque la notification de fin de flux a été envoyée, le convertisseur est dans un état d’attente ; Il est toujours en cours d’exécution, mais il est conscient qu’il ne recevra pas de données supplémentaires. Dans ces circonstances, le convertisseur dessine habituellement la zone de lecture en noir.

La gestion du vidage est une complication supplémentaire pour les convertisseurs. Le vidage est effectué via une paire de méthodes [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) appelée [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) et [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush). Le vidage est essentiellement un État supplémentaire qui doit être géré par le convertisseur. Il est interdit pour un filtre source d’appeler **BeginFlush** sans appeler **EndFlush**, si bien que l’État est short et discret. Toutefois, le convertisseur doit gérer correctement les données ou les notifications qu’il reçoit pendant la transition de vidage.

Toutes les données reçues après l’appel de [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) doivent être rejetées immédiatement en renvoyant **S \_ false**. En outre, toutes les notifications de fin de flux mises en cache doivent également être effacées lorsqu’un convertisseur est vidé. Un convertisseur est généralement vidé en réponse à une recherche. Le vidage garantit que les anciennes données sont effacées du graphique de filtre avant l’envoi des échantillons actualisés. (En général, la lecture de deux sections d’un flux, l’une après l’autre, est mieux gérée via des commandes différées plutôt que d’attendre la fin d’une section, puis d’émettre une commande Seek.)

## <a name="handling-state-changes-and-pause-completion"></a>Gestion des modifications d’État et suspension de la fin

Un filtre de convertisseur se comporte de la même façon que n’importe quel autre filtre dans le graphique de filtre quand son état est modifié, avec l’exception suivante. Après avoir été suspendue, le convertisseur aura des données mises en file d’attente, prêtes à être rendues lors de l’exécution ultérieure. Quand le convertisseur vidéo est arrêté, il conserve les données en file d’attente. Il s’agit d’une exception à la règle DirectShow qui indique qu’aucune ressource ne doit être maintenue par les filtres pendant l’arrêt du graphique de filtre.

La raison de cette exception est qu’en détenant des ressources, le convertisseur aura toujours une image avec laquelle redessiner la fenêtre si elle reçoit un message [**de \_ peinture WM**](/windows/desktop/gdi/wm-paint) . Elle dispose également d’une image pour satisfaire les méthodes, telles que [**CBaseControlVideo :: GetStaticImage**](cbasecontrolvideo-getstaticimage.md), qui demandent une copie de l’image actuelle. L’un des autres effets de la conservation des ressources est que la conservation de l’allocation empêche l’allocateur d’être dévalidée, ce qui à son tour rend le changement d’état suivant beaucoup plus rapide, car les mémoires tampons d’images sont déjà allouées.

Un convertisseur vidéo ne doit afficher et libérer des exemples qu’en cours d’exécution. Lorsqu’il est suspendu, le filtre peut les restituer (par exemple, lors du dessin d’une image d’affiche statique dans une fenêtre), mais ne doit pas les libérer. Les convertisseurs audio n’effectuent aucun rendu en pause (même s’ils peuvent exécuter d’autres activités, telles que la préparation du périphérique Wave, par exemple). L’heure à laquelle les exemples doivent être rendus est obtenue en combinant le temps de flux dans l’exemple avec le temps de référence passé comme paramètre à la méthode [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) . Les convertisseurs doivent rejeter les échantillons avec des heures de début inférieures ou égales aux heures de fin.

Quand une application suspend un graphique de filtre, le graphique de filtre ne retourne pas à partir de sa méthode [**IMediaControl ::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) jusqu’à ce que des données soient mises en file d’attente au niveau des convertisseurs. Pour ce faire, quand un convertisseur est suspendu, il doit retourner S \_ false s’il n’y a aucune donnée en attente d’être rendue. Si des données sont mises en file d’attente, elles peuvent retourner **S \_ OK**.

Le gestionnaire de graphique de filtre vérifie toutes les valeurs de retour lors de la suspension d’un graphique de filtre, pour s’assurer que les convertisseurs comportent des données mises en file d’attente. Si un ou plusieurs filtres ne sont pas prêts, le gestionnaire de graphes de filtres interroge les filtres dans le graphique en appelant [**IMediaFilter :: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate). La méthode **GetState** prend un paramètre de délai d’attente. Un filtre (en général un convertisseur) qui attend toujours l’arrivée des données avant de terminer la modification d’État retourne le niveau intermédiaire de l' **État de VFW \_ \_ \_ S** si la méthode **GetState** expire. Une fois que les données arrivent au convertisseur, **GetState** doit être renvoyé immédiatement avec la fonction **S \_ OK**.

Dans l’état intermédiaire et terminé, l’état du filtre signalé sera \_ suspendu. Seule la valeur de retour indique si le filtre est vraiment prêt ou non. Si, pendant qu’un convertisseur attend que les données arrivent, son filtre source envoie une notification de fin de flux, qui doit également terminer le changement d’État.

Une fois que tous les filtres ont des données en attente d’être rendues, le graphique de filtre termine le changement d’état de pause.

## <a name="handling-termination"></a>Gestion de l’arrêt

Les convertisseurs vidéo doivent gérer correctement les événements d’arrêt à partir de l’utilisateur. Cela implique de masquer correctement la fenêtre et de savoir comment faire si une fenêtre est forcée à être affichée par la suite. En outre, les convertisseurs vidéo doivent notifier le gestionnaire de graphique de filtre quand la fenêtre est détruite (ou plus précisément, lorsque le convertisseur est supprimé du graphique de filtre) pour libérer des ressources.

Si l’utilisateur ferme la fenêtre vidéo (par exemple en appuyant sur ALT + F4), la Convention consiste à masquer immédiatement la fenêtre et à envoyer une notification [**\_ USERABORT ce**](ec-userabort.md) au gestionnaire du graphique de filtres. Cette notification est transmise à l’application, ce qui entraîne l’arrêt de la diffusion du graphique. Après l’envoi de la **\_ USERABORT EC**, un convertisseur vidéo doit rejeter tous les échantillons supplémentaires qui lui sont livrés.

L’indicateur Graph-Stopped doit être laissé activé par le convertisseur jusqu’à ce qu’il soit arrêté par la suite. à partir de là, il doit être réinitialisé pour qu’une application puisse substituer l’action de l’utilisateur et poursuivre la diffusion du graphique si elle le souhaite. Si vous appuyez sur ALT + F4 pendant que la vidéo est en cours d’exécution, la fenêtre est masquée et tous les autres exemples livrés sont rejetés. Si la fenêtre est affichée par la suite (peut-être par le biais de [**IVideoWindow ::p ut \_ visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible)), aucune notification de [**\_ redessin ce**](ec-repaint.md) ne doit être générée.

Le convertisseur vidéo doit également envoyer la notification [**\_ \_ détruite de la fenêtre EC**](ec-window-destroyed.md) au graphique de filtre lorsque le convertisseur vidéo se termine. En fait, il est préférable de gérer cela quand la méthode [**IBaseFilter :: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) du convertisseur est appelée avec un paramètre null (indiquant que le convertisseur est sur le point d’être supprimé du graphique de filtre), au lieu d’attendre la destruction de la fenêtre vidéo réelle. L’envoi de cette notification permet au serveur de distribution du plug-in du gestionnaire de graphes de filtrer de transmettre les ressources qui dépendent du focus de la fenêtre vers d’autres filtres, tels que les périphériques audio.

## <a name="handling-dynamic-format-changes"></a>Gestion des modifications de format dynamique

Dans certains cas, le filtre amont du convertisseur peut tenter de modifier le format vidéo pendant la diffusion de la vidéo. Il s’agit le plus souvent du Décompresseur vidéo qui lance une modification de format dynamique.

Un filtre amont tentant de modifier les formats de manière dynamique doit toujours appeler la méthode [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur la broche d’entrée du convertisseur. Un convertisseur vidéo a une certaine liberté quant aux types de modifications de format dynamique qu’il doit prendre en charge. Au minimum, il doit autoriser le filtre en amont à modifier les palettes. Lorsqu’un filtre amont change de type de média, il joint le type de média au premier exemple fourni dans le nouveau format. Si le convertisseur contient des exemples dans une file d’attente pour le rendu, il ne doit pas modifier le format tant qu’il n’a pas rendu l’exemple avec la modification de type.

Un convertisseur vidéo peut également demander une modification de format à partir du décodeur. Par exemple, il peut demander au décodeur de fournir un format compatible DirectDraw avec une **bihauteur** négative. Quand le convertisseur est suspendu, il doit appeler [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur le code confidentiel amont pour voir quels formats le décodeur peut fournir. Le décodeur peut toutefois ne pas énumérer tous les types qu’il peut accepter, de sorte que le convertisseur doit proposer certains types même si le décodeur ne les publie pas.

Si le décodeur peut basculer vers le format demandé, il retourne **S \_ OK** à partir de [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept). Le convertisseur associe ensuite le nouveau type de média à l’exemple de support suivant sur l’allocateur en amont. Pour que cela fonctionne, le convertisseur doit fournir un allocateur personnalisé qui implémente une méthode privée pour attacher le type de média à l’exemple suivant. (Dans cette méthode privée, appelez [**IMediaSample :: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) pour définir le type.)

La broche d’entrée du convertisseur doit retourner l’allocateur personnalisé du convertisseur dans la méthode [**IMemInputPin :: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) . Remplacez [**IMemInputPin :: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) afin qu’il échoue si le filtre amont n’utilise pas l’allocateur du convertisseur.

Avec certains décodeurs, le fait de définir la **bihauteur** sur un nombre positif sur les types YUV fait que le décodeur dessine l’image à l’envers. (Cette erreur est incorrecte et doit être considérée comme un bogue dans le décodeur.)

Chaque fois qu’une modification de format est détectée par le convertisseur vidéo, elle doit envoyer une notification de [**\_ \_ modification d’affichage EC**](ec-display-changed.md) . La plupart des convertisseurs vidéo sélectionnent un format pendant la connexion afin que le format puisse être dessiné efficacement via GDI. Si l’utilisateur modifie le mode d’affichage actuel sans redémarrer l’ordinateur, un convertisseur peut se retrouver avec une connexion de format d’image incorrecte et doit envoyer cette notification. Le premier paramètre doit être le code confidentiel qui doit se reconnecter. Le gestionnaire de graphes de filtre s’arrange pour que le graphique de filtre soit arrêté et le code confidentiel reconnecté. Lors de la reconnexion suivante, le convertisseur peut accepter un format plus approprié.

Chaque fois qu’un convertisseur vidéo détecte une modification de la palette dans le flux, il doit envoyer la notification de [**\_ \_ modification de la palette EC**](ec-palette-changed.md) au gestionnaire du graphique de filtres. Les convertisseurs vidéo DirectShow détectent si une palette a vraiment changé dans le format dynamique. Les convertisseurs vidéo permettent non seulement de filtrer le nombre de notifications **\_ \_ modifiées de palette EC** envoyées, mais également de réduire la quantité de création, d’installation et de suppression de palettes requises.

Enfin, le convertisseur vidéo peut également détecter que la taille de la vidéo a changé. dans ce cas, il doit envoyer la notification [**de \_ \_ \_ modification**](ec-video-size-changed.md) de la taille de la vidéo ce. Une application peut utiliser cette notification pour négocier de l’espace dans un document composé. Les dimensions vidéo réelles sont disponibles via l’interface de contrôle [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . Les convertisseurs DirectShow détectent si la vidéo a changé de taille ou non avant d’envoyer ces événements.

## <a name="handling-persistent-properties"></a>Gestion des propriétés persistantes

Toutes les propriétés définies par le biais des interfaces [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) et [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) sont destinées à être persistantes entre les connexions. Par conséquent, la déconnexion et la reconnexion d’un convertisseur doivent n’afficher aucun effet sur la taille, la position ou les styles de la fenêtre. Toutefois, si les dimensions de la vidéo changent entre les connexions, le convertisseur doit réinitialiser les rectangles source et de destination à leurs valeurs par défaut. Les positions source et de destination sont définies par le biais de l’interface **IBasicVideo** .

[**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) et [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) fournissent un accès suffisant aux propriétés pour permettre à une application d’enregistrer et de restaurer toutes les données dans l’interface dans un format persistant. Cela s’avère utile pour les applications qui doivent enregistrer la configuration exacte et les propriétés des graphiques de filtre au cours d’une session d’édition et les restaurer ultérieurement.

## <a name="handling-ec_repaint-notifications"></a>Gestion des \_ notifications de REDESSIN ce

La notification de [**\_ redessin ce**](ec-repaint.md) est envoyée uniquement lorsque le convertisseur est suspendu ou arrêté. Cette notification signale au gestionnaire de graphique de filtre que le convertisseur a besoin de données. Si le graphique de filtre est arrêté lorsqu’il reçoit l’une de ces notifications, il suspend le graphique de filtre, attend que tous les filtres reçoivent des données (en appelant [**GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)), puis l’arrête à nouveau. Lorsqu’il est arrêté, un convertisseur vidéo doit conserver l’image afin que les messages [**de \_ peinture WM**](/windows/desktop/gdi/wm-paint) suivants puissent être gérés.

Par conséquent, si un convertisseur vidéo reçoit un message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) lorsqu’il est arrêté ou suspendu, et qu’il n’a rien à faire pour peindre sa fenêtre, il doit l’envoyer au gestionnaire de graphes [**de filtre \_**](ec-repaint.md) . Si une notification de **\_ redessin ce** a été reçue pendant la suspension, le gestionnaire de graphique de filtre appelle [**IMediaPosition ::p ut \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) avec la position actuelle (c’est-à-dire, cherche à la position actuelle). Ainsi, les filtres sources vident le graphique de filtre et entraînent l’envoi de nouvelles données via le graphique de filtre.

Un convertisseur ne doit envoyer qu’une seule de ces notifications à la fois. Par conséquent, une fois que le convertisseur envoie une notification, il doit s’assurer qu’aucun autre n’est envoyé jusqu’à la remise de certains échantillons. La méthode conventionnelle pour effectuer cette opération consiste à avoir un indicateur qui indique qu’un redessin peut être envoyé, ce qui est désactivé après l’envoi d’une notification de [**\_ redessin ce**](ec-repaint.md) . Cet indicateur doit être réinitialisé une fois que les données sont remises ou lorsque la broche d’entrée est vidée, mais pas si la fin de flux est signalée sur la broche d’entrée.

Si le convertisseur ne surveille pas ses notifications de [**\_ redessin EC**](ec-repaint.md) , il inondera le gestionnaire de graphes de filtre avec les demandes de **\_ redessin EC** (qui sont relativement coûteuses à traiter). Par exemple, si un convertisseur n’a pas d’image à dessiner et qu’une autre fenêtre est glissée dans la fenêtre du convertisseur dans une opération de glissement complet, le convertisseur reçoit plusieurs [**messages \_ WM**](/windows/desktop/gdi/wm-paint) . Seule la première d’entre elles doit générer une notification d’événement de **\_ redessin ce** à partir du convertisseur vers le gestionnaire de graphes de filtre.

Un convertisseur doit envoyer sa broche d’entrée en tant que premier paramètre à la notification de [**\_ redessin ce**](ec-repaint.md) . En procédant ainsi, la broche de sortie attachée sera interrogée pour [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)et, si elle est prise en charge, la notification **ce \_ Repaint** sera envoyée pour la première fois. Cela permet aux broches de sortie de gérer les redessins avant que le graphique de filtre ne soit manipulé. Cela ne sera pas effectué si le graphique de filtre est arrêté, car aucune mémoire tampon n’est disponible à partir de l’allocateur de convertisseur non validé.

Si la broche de sortie ne peut pas gérer la demande et que le graphique de filtre est en cours d’exécution, la notification [**ce \_ Repaint**](ec-repaint.md) est ignorée. Une broche de sortie doit retourner **S \_ OK** à partir de [**IMediaEventSink :: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) pour signaler qu’elle a correctement traité la demande de Repaint. La broche de sortie sera appelée sur le thread de travail du gestionnaire de graphique de filtre, ce qui évite que le convertisseur n’appelle la broche de sortie directement, ce qui contourner tous les problèmes de blocage. Si le graphique de filtre est arrêté ou suspendu et que la sortie ne gère pas la demande, le traitement par défaut est effectué.

## <a name="handling-notifications-in-full-screen-mode"></a>Gestion des notifications en mode Full-Screen

Le serveur de distribution de plug-in [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) dans le graphique de filtre gère la lecture en plein écran. Il permutera un convertisseur vidéo en sortie pour un convertisseur plein écran spécialisé, étirer une fenêtre d’un convertisseur en plein écran, ou faire en sorte que le convertisseur implémente directement la lecture en plein écran. Pour interagir avec les protocoles plein écran, un convertisseur vidéo doit envoyer une notification [**d' \_ activation EC**](ec-activate.md) chaque fois que sa fenêtre est activée ou désactivée. En d’autres termes, une notification d' **\_ activation EC** doit être envoyée pour chaque \_ message WM ACTIVATEAPP reçu par un convertisseur.

Lorsqu’un convertisseur est utilisé en mode plein écran, ces notifications gèrent le basculement vers et à partir de ce mode plein écran. La désactivation de la fenêtre se produit généralement lorsqu’un utilisateur appuie sur ALT + TAB pour basculer vers une autre fenêtre, que le convertisseur de l’écran complet DirectShow utilise comme signal pour revenir au mode de rendu standard.

Lorsque la notification d' [**\_ activation ce**](ec-activate.md) est envoyée au gestionnaire de graphique de filtre lors du basculement en mode plein écran, le gestionnaire de graphes de filtre envoie une notification de [**\_ \_ perte**](ec-fullscreen-lost.md) de la mise en plein écran à l’application de contrôle. L’application peut utiliser cette notification pour restaurer l’état d’un bouton plein écran, par exemple. Les notifications d' **\_ activation EC** sont utilisées en interne par DirectShow pour gérer le basculement plein écran sur les signaux des convertisseurs vidéo.

## <a name="summary-of-notifications"></a>Résumé des notifications

Cette section répertorie les notifications de graphique de filtre qu’un convertisseur peut envoyer.



| Notification d'événement                                        | Description                                                                                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_activation EC**](ec-activate.md)                       | Envoyé par les convertisseurs vidéo en mode de rendu plein écran pour chaque \_ message WM ACTIVATEAPP reçu.                                                                                                  |
| [**EC \_ complet**](ec-complete.md)                       | Envoyé par les convertisseurs une fois que toutes les données ont été rendues.                                                                                                                                               |
| [**\_affichage EC \_ modifié**](ec-display-changed.md)        | Envoyé par les convertisseurs vidéo en cas de modification du format d’affichage.                                                                                                                                            |
| [**\_palette EC \_ modifiée**](ec-palette-changed.md)        | Envoyé chaque fois qu’un convertisseur vidéo détecte une modification de la palette dans le flux.                                                                                                                            |
| [**redessin ce \_**](ec-repaint.md)                         | Envoyé par les convertisseurs vidéo arrêtés ou suspendus lorsqu’un \_ message de peinture WM est reçu et qu’il n’y a pas de données à afficher. Le gestionnaire de graphes de filtre génère alors un cadre pour peindre à l’écran. |
| [**\_USERABORT EC**](ec-userabort.md)                     | Envoyé par les convertisseurs vidéo pour signaler une fermeture que l’utilisateur a demandée (par exemple, un utilisateur qui ferme la fenêtre vidéo).                                                                               |
| [**taille de la \_ vidéo ce \_ \_ modifiée**](ec-video-size-changed.md) | Envoyé par les convertisseurs vidéo chaque fois qu’une modification de la taille de la vidéo native est détectée.                                                                                                                       |
| [**\_fenêtre EC \_ détruite**](ec-window-destroyed.md)      | Envoyé par les convertisseurs vidéo lorsque le filtre est supprimé ou détruit afin que les ressources qui dépendent du focus de la fenêtre puissent être passées à d’autres filtres.                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture de convertisseurs vidéo](writing-video-renderers.md)
</dt> </dl>

 

 
