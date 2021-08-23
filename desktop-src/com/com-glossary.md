---
title: Glossaire COM
description: Page de glossaire
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e2c56a2-0572-48b6-a2ef-650f1cf1b62e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0c4c1aa78c81484666311dfcdd6bae8b4e6daaa45581af98f50171f48b4b58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048507"
---
# <a name="com-glossary"></a>Glossaire COM

<dl> <dt>

<span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**actionne**
</dt> <dd>

Processus de chargement d’un objet en mémoire, qui le met à l’État en cours d’exécution.

</dd> <dt>

<span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**État actif**
</dt> <dd>

Objet COM qui est à l’État en cours d’exécution et qui a une interface utilisateur visible.

</dd> <dt>

<span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**moniker absolu**
</dt> <dd>

Moniker qui spécifie l’emplacement absolu d’un objet. Un moniker absolu est analogue à un chemin d’accès complet.

</dd> <dt>

<span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**détenteur de la notification**
</dt> <dd>

Objet COM qui met en cache, gère et envoie des notifications de modifications aux récepteurs de notifications des applications de conteneur.

</dd> <dt>

<span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**récepteur de notifications**
</dt> <dd>

Objet COM qui peut recevoir des notifications de modifications dans un objet incorporé ou lié, car il implémente l’interface [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) ou [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) . Les conteneurs qui doivent être avertis des modifications apportées aux objets implémentent un récepteur de notifications. Les notifications proviennent du serveur, qui utilise un objet de détenteur de notifications pour mettre en cache et gérer les notifications aux conteneurs.

</dd> <dt>

<span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**Aggregate (objet)**
</dt> <dd>

Objet COM qui est constitué d’un ou de plusieurs autres objets COM. Un objet de l’agrégat est désigné comme l’objet de contrôle, qui contrôle les interfaces de l’agrégat qui sont exposées et qui sont privées. Cet objet de contrôle a une implémentation spéciale de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , appelée **IUnknown** de contrôle. Tous les objets de l’agrégat doivent passer des appels aux méthodes **IUnknown** via le contrôle **IUnknown**.

</dd> <dt>

<span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**agréger**
</dt> <dd>

Technique de composition pour l’implémentation d’objets COM. Elle vous permet de générer un nouvel objet en réutilisant une ou plusieurs implémentations d’interface d’objets existantes. L’objet d’agrégation choisit les interfaces à exposer aux clients, et les interfaces sont exposées comme si elles étaient implémentées par l’objet d’agrégation. Les clients de l’objet d’agrégation communiquent uniquement avec l’objet d’agrégation.

</dd> <dt>

<span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**propriété ambiante**
</dt> <dd>

Propriété au moment de l’exécution qui est gérée et exposée par le conteneur. En règle générale, une propriété ambiante représente une caractéristique d’un formulaire, telle que la couleur d’arrière-plan, qui doit être communiquée à un contrôle afin que le contrôle puisse assumer l’apparence de son environnement environnant.

</dd> <dt>

<span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**anti-moniker**
</dt> <dd>

Inverse d’un moniker de fichier, d’élément ou de pointeur. Un anti-moniker est ajouté à la fin d’un fichier, d’un élément ou d’un moniker de pointeur pour l’annuler. Les anti-monikers sont utilisés dans la construction de monikers relatifs.

</dd> <dt>

<span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**décompte de références artificielles**
</dt> <dd>

Technique utilisée pour protéger un objet avant d’appeler une fonction ou une méthode qui pourrait le détruire prématurément. Un programme appelle **IUnknown :: AddRef** pour incrémenter le décompte de références de l’objet avant d’effectuer l’appel qui pourrait libérer l’objet. Une fois que la fonction a retourné une valeur, le programme appelle **IUnknown :: Release** pour décrémenter le nombre.

</dd> <dt>

<span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**liaison asynchrone**
</dt> <dd>

Type de liaison dans laquelle il est nécessaire que le processus se produise de façon asynchrone afin d’éviter une dégradation des performances pour l’utilisateur final. En règle générale, la liaison asynchrone est utilisée dans les environnements distribués tels que le World Wide Web. OLE prend en charge les classes de moniker asynchrones et les mécanismes de rappel qui permettent au processus de localisation et d’initialisation d’un objet dans un environnement distribué de se produire pendant l’exécution d’autres opérations.

</dd> <dt>

<span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**appel asynchrone**
</dt> <dd>

Appel à une fonction exécutée séparément afin que l’appelant puisse continuer à traiter les instructions sans attendre le retour de la fonction.

</dd> <dt>

<span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**moniker asynchrone**
</dt> <dd>

Moniker qui prend en charge la liaison asynchrone. Par exemple, les instances de la classe moniker d’URL fournie par le système sont des monikers asynchrones.

</dd> <dt>

<span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**mati**
</dt> <dd>

Moyen de manipuler les objets d’une application à partir de l’extérieur de l’application. Automation est généralement utilisé pour créer des applications qui exposent des objets à des outils de programmation et des langages de macro, pour créer et manipuler des objets d’une application à partir d’autres applications, ou pour créer des outils permettant d’accéder aux objets et de les manipuler.

</dd> <dt>

<span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**contexte de liaison**
</dt> <dd>

Objet COM qui implémente l’interface [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) . Les contextes de liaison sont utilisés dans les opérations de moniker pour contenir des références aux objets activés lorsqu’un moniker est lié. Le contexte de liaison contient des paramètres qui s’appliquent à toutes les opérations pendant la liaison d’un moniker composite générique et fournit l’implémentation du moniker avec un accès aux informations sur son environnement.

</dd> <dt>

<span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**liant**
</dt> <dd>

Association d’un nom à son référent. En particulier, en localisant l’objet nommé par un moniker, en le plaçant dans son état d’exécution s’il n’est pas déjà, et en retournant un pointeur d’interface vers celui-ci. Les objets peuvent être liés au moment de l’exécution (également appelé liaison tardive ou liaison dynamique) ou au moment de la compilation (également appelé liaison statique).

</dd> <dt>

<span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**en**
</dt> <dd>

Magasin d’informations local (généralement temporaire). Dans OLE, un cache contient des informations qui définissent la présentation d’un objet lié ou incorporé lorsque le conteneur est ouvert.

</dd> <dt>

<span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**initialisation du cache**
</dt> <dd>

Remplissage du cache d’un objet lié ou incorporé avec les données de présentation. L’interface [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) fournit des méthodes qu’un conteneur peut appeler pour contrôler les données mises en cache pour les objets liés ou incorporés.

</dd> <dt>

<span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**type**
</dt> <dd>

Définition d’un objet dans le code. En C++, la classe d’un objet est définie comme un type de données, mais ce n’est pas le cas dans d’autres langages. Étant donné que OLE peut être codé dans n’importe quel langage, la classe est utilisée pour faire référence à la définition générale de l’objet.

</dd> <dt>

<span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**fabrique de classes**
</dt> <dd>

Objet COM qui implémente l’interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) et qui crée une ou plusieurs instances d’un objet identifié par un identificateur de classe (CLSID) donné.

</dd> <dt>

<span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**identificateur de classe (CLSID)**
</dt> <dd>

Identificateur global unique (GUID) associé à un objet de classe OLE. Si un objet de classe sera utilisé pour créer plusieurs instances d’un objet, l’application serveur associée doit inscrire son CLSID dans le registre système afin que les clients puissent localiser et charger le code exécutable associé aux objets. Chaque serveur ou conteneur OLE qui autorise la liaison à ses objets incorporés doit inscrire un CLSID pour chaque définition d’objet prise en charge.

</dd> <dt>

<span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**objet de classe**
</dt> <dd>

Dans la programmation orientée objet, objet dont l’État est partagé par tous les objets d’une classe et dont le comportement agit sur ces données d’État classwide. Dans COM, les objets de classe sont appelés fabriques de classes et n’ont généralement aucun comportement à l’exception de la création de nouvelles instances de la classe.

</dd> <dt>

<span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**client**
</dt> <dd>

Objet COM qui demande des services à partir d’un autre objet.

</dd> <dt>

<span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**site client**
</dt> <dd>

Site d’affichage d’un objet incorporé ou lié dans un document composé. Le site client est le principal moyen par lequel un objet demande des services à partir de son conteneur.

</dd> <dt>

<span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**IDENTIFICATEUR**
</dt> <dd>

Identificateur global unique (GUID) associé à un objet de classe OLE. Si un objet de classe sera utilisé pour créer plusieurs instances d’un objet, l’application serveur associée doit inscrire son CLSID dans le registre système afin que les clients puissent localiser et charger le code exécutable associé aux objets. Chaque serveur ou conteneur OLE qui autorise la liaison à ses objets incorporés doit inscrire un CLSID pour chaque définition d’objet prise en charge.

</dd> <dt>

<span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**valider**
</dt> <dd>

Pour enregistrer de façon permanente toute modification apportée à un objet de stockage ou de flux depuis son ouverture ou lors du dernier enregistrement des modifications.

</dd> <dt>

<span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**-**
</dt> <dd>

Objet qui encapsule les données et le code, et fournit un ensemble bien spécifié de services disponibles publiquement.

</dd> <dt>

<span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**COM (Component Object Model)**
</dt> <dd>

Le modèle de programmation orienté objet OLE qui définit la façon dont les objets interagissent au sein d’un même processus ou entre des processus. Dans COM, les clients ont accès à un objet via des interfaces implémentées sur l’objet.

</dd> <dt>

<span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**barre de menus composite**
</dt> <dd>

Barre de menus partagée composée de groupes de menus issus d’une application de conteneur et d’une application serveur activée sur place.

</dd> <dt>

<span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**moniker composite**
</dt> <dd>

Moniker qui se compose de deux monikers ou plus qui sont traités comme une unité. Un moniker composite peut être non générique, ce qui signifie que ses monikers de composants ont une connaissance particulière de l’un l’autre, ou générique, ce qui signifie que ses monikers de composants ne savent rien de l’autre, sauf qu’il s’agit de monikers

</dd> <dt>

<span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**document composé**
</dt> <dd>

Document qui comprend des objets liés ou incorporés, ainsi que ses propres données natives.

</dd> <dt>

<span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**fichier composé**
</dt> <dd>

implémentation de Stockage structurée fournie par OLE.

</dd> <dt>

<span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**Objet COM**
</dt> <dd>

Objet qui est conforme au modèle COM (Component Object Model) OLE. Un objet COM est une instance d’une définition d’objet, qui spécifie les données de l’objet et une ou plusieurs implémentations d’interfaces sur l’objet. Les clients interagissent avec un objet COM uniquement par le biais de ses interfaces.

</dd> <dt>

<span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**objet connectable**
</dt> <dd>

Objet COM qui implémente, au minimum, l’interface [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) , pour la gestion des objets de point de connexion. Les objets connectables prennent en charge la communication entre le serveur et le client. Un objet connectable crée et gère un ou plusieurs sous-objets de point de connexion qui reçoivent des événements des interfaces implémentées sur d’autres objets et les envoient au client.

</dd> <dt>

<span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**objet point de connexion**
</dt> <dd>

Objet COM géré par un objet connectable et qui implémente l’interface [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) . Un ou plusieurs objets point de connexion peuvent être créés et gérés par un objet connectable. Chaque objet de point de connexion gère les événements entrants à partir d’une interface spécifique sur un autre objet et envoie ces événements au client.

</dd> <dt>

<span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**application de conteneur**
</dt> <dd>

Application qui prend en charge les documents composés. L’application de conteneur fournit un stockage pour un objet incorporé ou lié, un site pour son affichage, un accès au site d’affichage et un récepteur de notifications pour recevoir des notifications de modifications de l’objet.

</dd> <dt>

<span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**imbrication**
</dt> <dd>

Technique de composition pour l’implémentation d’objets COM. Il permet à un objet de réutiliser une partie ou la totalité des implémentations d’interface d’un ou plusieurs autres objets. L’objet externe agit comme un client pour les autres objets, en déléguant l’implémentation lorsqu’il souhaite utiliser les services de l’un des objets contenus.

</dd> <dt>

<span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**contexte**
</dt> <dd>

Dans COM+, ensemble de propriétés d’exécution associées à un ou plusieurs objets COM utilisés pour fournir des services pour ces objets.

</dd> <dt>

<span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**régulation**
</dt> <dd>

Objet COM incorporable et réutilisable qui prend en charge, au minimum, l’interface [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) . Les contrôles sont généralement associés à l’interface utilisateur. Elles prennent également en charge la communication avec un conteneur et peuvent être réutilisées par plusieurs clients, en fonction des critères de licence.

</dd> <dt>

<span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**conteneur de contrôle**
</dt> <dd>

Application qui prend en charge l’incorporation de contrôles en implémentant l’interface [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) .

</dd> <dt>

<span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**Control, propriété**
</dt> <dd>

Propriété au moment de l’exécution qui est exposée et gérée par le contrôle lui-même. Par exemple, la taille de police et de texte utilisée par le contrôle sont des propriétés de contrôle.

</dd> <dt>

<span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**contrôle de l’objet**
</dt> <dd>

Objet dans un objet d’agrégation qui contrôle les interfaces de l’objet d’agrégation qui sont exposées et qui sont privées. L’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de l’objet de contrôle est appelée **IUnknown** de contrôle. Les appels aux méthodes **IUnknown** des autres objets de l’agrégat doivent être passés au contrôle **IUnknown**.

</dd> <dt>

<span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**site de contrôle**
</dt> <dd>

Structure implémentée par un conteneur de contrôle pour gérer l’affichage et le stockage d’un contrôle. Dans un conteneur donné, chaque contrôle dispose d’un site de contrôle correspondant.

</dd> <dt>

<span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**objet de transfert de données**
</dt> <dd>

Objet qui implémente l’interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) et contient les données à transférer d’un objet à un autre par le biais du presse-papiers ou des opérations de glisser-déplacer.

</dd> <dt>

<span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**gestionnaire d’objets par défaut**
</dt> <dd>

DLL fournie avec OLE qui agit comme un substitut dans l’espace de traitement de l’application conteneur pour l’objet réel.

Avec le gestionnaire d’objets par défaut, il est possible d’examiner les données stockées d’un objet sans réellement activer l’objet. Le gestionnaire d’objets par défaut effectue d’autres tâches, telles que le rendu d’un objet à partir de son état mis en cache lorsque l’objet est chargé en mémoire.

</dd> <dt>

<span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**objet dépendant**
</dt> <dd>

Objet COM qui est généralement initialisé par un autre objet (l’objet hôte). Bien que la durée de vie des objets dépendants ne soit utile que pendant la durée de vie de l’objet hôte, l’objet hôte ne fonctionne pas comme le contrôle [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pour l’objet dépendant. En revanche, un objet est un objet agrégé lorsque sa durée de vie (au moyen de son décompte de références) est complètement contrôlé par l’objet de gestion.

</dd> <dt>

<span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**mode d’accès direct**
</dt> <dd>

Un des deux modes d’accès dans lesquels un objet de stockage peut être ouvert. En mode direct, toutes les modifications sont immédiatement validées sur l’objet de stockage racine.

</dd> <dt>

<span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**objet document**
</dt> <dd>

Document OLE qui peut afficher une ou plusieurs vues activées sur place de ses données dans un frame natif ou étranger, tel qu’un navigateur, tout en conservant le contrôle total sur son interface utilisateur. Outre l’implémentation du document OLE habituel et des interfaces d’activation sur place, un objet document doit implémenter [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument), et chacune de ses vues (sous la forme d’un objet de vue de document) doit implémenter [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).

</dd> <dt>

<span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**conteneur d’objets de document**
</dt> <dd>

Application conteneur qui permet d’afficher une ou plusieurs vues d’un ou plusieurs objets document et de gérer tous les objets de document contenus dans un fichier. Chaque objet de document est associé à un site de document, et chaque site de document contient un ou plusieurs sites d’affichage de documents correspondant aux vues prises en charge par l’objet de document. Un conteneur d’objets de document comprend également un frame de conteneur, qui gère la négociation des menus et des barres d’outils, ainsi que l’énumération des objets contenus.

</dd> <dt>

<span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**serveur d’objets de document**
</dt> <dd>

Application serveur qui permet de fournir des objets de document.

</dd> <dt>

<span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**site de document**
</dt> <dd>

Site client implémenté par un conteneur d’objets de document pour gérer l’affichage et le stockage d’un objet de document. Chaque objet de document dans un conteneur a un site de document correspondant.

</dd> <dt>

<span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**objet site de document**
</dt> <dd>

Objet COM qui implémente l’interface [**IOleDocumentSite**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) , en plus des interfaces de site client habituelles (telles que [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).

</dd> <dt>

<span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**vue de document**
</dt> <dd>

Présentation particulière des données d’un document. Un objet document unique peut avoir un ou plusieurs affichages, mais un seul affichage de document peut appartenir à un seul objet document.

</dd> <dt>

<span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**objet de vue de document**
</dt> <dd>

Objet COM qui implémente l’interface [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) et qui correspond à une vue de document particulière. Un objet avec plusieurs vues de document agrège un objet d’affichage de document distinct pour chaque vue.

</dd> <dt>

<span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**site d’affichage de documents**
</dt> <dd>

Objet agrégé par un objet site de document pour gérer l’espace d’affichage d’une vue particulière d’un objet document. Dans un site de document donné, chaque vue de document a un site d’affichage de documents correspondant.

</dd> <dt>

<span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**objet de site d’affichage de document**
</dt> <dd>

Objet COM qui est agrégé dans un objet de site de document et implémente l’interface [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) et, éventuellement, l’interface [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) .

</dd> <dt>

<span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**glisser-déplacer**
</dt> <dd>

Opération dans laquelle l’utilisateur final utilise la souris ou un autre dispositif de pointage pour déplacer des données vers un autre emplacement dans la même fenêtre ou dans une autre fenêtre.

</dd> <dt>

<span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**Incorporer**
</dt> <dd>

Insérer un objet dans un document composé de manière à conserver les formats de données natifs de cet objet et à l’autoriser à être modifié à partir de son conteneur à l’aide d’outils exposés par son serveur.

</dd> <dt>

<span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**objet incorporé**
</dt> <dd>

Objet dont les données sont stockées dans un document composé, mais l’objet s’exécute dans l’espace de processus de son serveur. Le gestionnaire d’objets par défaut fournit un substitut dans l’espace de traitement de l’application conteneur pour l’objet réel.

</dd> <dt>

<span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**propriété étendue**
</dt> <dd>

Une propriété au moment de l’exécution, telle que la position et la taille d’un contrôle, qu’un utilisateur peut supposer être exposée par le contrôle, mais qui est exposée et gérée par le conteneur.

</dd> <dt>

<span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**moniker de fichier**
</dt> <dd>

Moniker basé sur un chemin d’accès dans le système de fichiers. Les monikers de fichiers peuvent être utilisés pour identifier les objets enregistrés dans leurs propres fichiers. Un moniker de fichier est un objet COM qui prend en charge l’implémentation fournie par le système de l’interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) pour la classe moniker de fichier.

</dd> <dt>

<span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**objet font**
</dt> <dd>

Objet COM qui fournit l’accès aux polices Graphics Device Interface (GDI) en implémentant l’interface [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) .

</dd> <dt>

<span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**identificateur de format**
</dt> <dd>

GUID qui identifie un jeu de propriétés persistantes. Également appelé FMTID.

</dd> <dt>

<span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**Frame**
</dt> <dd>

Partie d’une application de conteneur responsable de la négociation des menus, des touches accélérateur, des barres d’outils et d’autres éléments partagés de l’interface utilisateur avec un objet COM incorporé ou un objet document.

</dd> <dt>

<span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**objet Frame**
</dt> <dd>

Objet COM qui implémente l’interface [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) et, éventuellement, l’interface [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) .

</dd> <dt>

<span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**moniker composite générique**
</dt> <dd>

Collection séquencée de monikers, en commençant par un moniker de fichier pour fournir le chemin d’accès au niveau du document et en continuant avec un ou plusieurs monikers d’élément qui, pris dans son ensemble, identifient un objet de manière unique.

</dd> <dt>

<span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**fonction d’assistance**
</dt> <dd>

Fonction qui encapsule les appels à d’autres fonctions et méthodes d’interface accessibles publiquement dans le kit de développement logiciel (SDK) OLE. Les fonctions d’assistance sont un moyen pratique d’appeler des séquences fréquemment utilisées d’appels de fonction et de méthode qui accomplissent des tâches courantes.

</dd> <dt>

<span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**objet hôte**
</dt> <dd>

Objet COM qui forme une relation hiérarchique avec un ou plusieurs autres objets COM, appelés objets dépendants. En règle générale, l’objet hôte instancie les objets dépendants, et leur existence n’est utile que dans la durée de vie de l’objet hôte. Toutefois, l’objet hôte n’agit pas comme le contrôle [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pour les objets dépendants, pas plus qu’il ne délègue directement aux implémentations d’interface de ces objets.

</dd> <dt>

<span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**SIGNÉ**
</dt> <dd>

Une poignée de résultat opaque définie comme égale à zéro pour un retour réussi d’une fonction et une valeur différente de zéro si des informations d’erreur ou d’État sont retournées.

</dd> <dt>

<span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**objet Hyperlink**
</dt> <dd>

Objet COM qui implémente, au minimum, l’interface [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) et agit comme un lien vers un objet à un autre emplacement (la cible). Un lien hypertexte est constitué de quatre parties : un moniker qui identifie l’emplacement de la cible ; chaîne pour l’emplacement dans la cible ; nom convivial ou affichable pour la cible ; et une chaîne qui peut contenir des paramètres supplémentaires.

</dd> <dt>

<span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**contexte de navigation de lien hypertexte**
</dt> <dd>

Objet COM qui implémente l’interface [**IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) et gère la pile de navigation de lien hypertexte. L’objet de contexte de navigation gère la fenêtre frame de lien hypertexte et la fenêtre de l’objet de cible de lien hypertexte.

</dd> <dt>

<span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**conteneur de liens hypertexte**
</dt> <dd>

Application conteneur qui prend en charge les liens hypertexte en implémentant l’interface [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) et, si les objets du conteneur peuvent être des cibles d’autres liens hypertexte, l’interface [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) .

</dd> <dt>

<span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**objet de frame de lien hypertexte**
</dt> <dd>

Objet COM qui implémente l’interface [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) et contrôle la navigation et l’affichage de niveau supérieur des liens hypertexte pour le conteneur du frame et le serveur de la cible du lien hypertexte.

</dd> <dt>

<span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**objet de site de lien hypertexte**
</dt> <dd>

Objet COM qui implémente l’interface [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) et fournit soit le moniker, soit l’identificateur d’interface de son conteneur de liens hypertexte. Un site de liens hypertexte peut traiter plusieurs liens hypertexte.

</dd> <dt>

<span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**objet de cible de lien hypertexte**
</dt> <dd>

Objet COM qui implémente l’interface [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) et fournit son moniker, son nom convivial et d’autres informations que d’autres objets Hyperlink utiliseront pour y accéder.

</dd> <dt>

<span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**dans le paramètre**
</dt> <dd>

Paramètre qui est alloué, défini et libéré par l’appelant d’une fonction ou d’une méthode d’interface. Un paramètre in n’est pas modifié par la fonction appelée.

</dd> <dt>

<span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**paramètre in/out**
</dt> <dd>

Paramètre qui est initialement alloué par l’appelant d’une fonction ou d’une méthode d’interface, et défini, libéré et réalloué, si nécessaire, par le processus appelé.

</dd> <dt>

<span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**activation sur place**
</dt> <dd>

Modification d’un objet incorporé dans la fenêtre de son conteneur à l’aide des outils fournis par le serveur. Les objets liés ne prennent pas en charge l’activation sur place ; ils sont toujours modifiés dans la fenêtre du serveur.

</dd> <dt>

<span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**serveur in-process**
</dt> <dd>

Serveur implémenté comme une DLL qui s’exécute dans l’espace de processus du client.

</dd> <dt>

<span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**instancié**
</dt> <dd>

Objet pour lequel la mémoire est allouée ou qui est persistante.

</dd> <dt>

<span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**interface**
</dt> <dd>

Groupe de fonctions sémantiquement associées qui fournissent l’accès à un objet COM. Chaque interface OLE définit un contrat qui autorise les objets à interagir en fonction du modèle COM (Component Object Model). Bien que OLE fournisse de nombreuses implémentations d’interface, la plupart des interfaces peuvent également être implémentées par les développeurs qui conçoivent des applications OLE.

</dd> <dt>

<span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**identificateur d’interface (IID)**
</dt> <dd>

Identificateur global unique (GUID) associé à une interface. Certaines fonctions prennent les IID comme paramètres pour permettre à l’appelant de spécifier le pointeur d’interface qui doit être retourné.

</dd> <dt>

<span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**moniker d’élément**
</dt> <dd>

Moniker basé sur une chaîne qui identifie un objet dans un conteneur. Les monikers d’élément peuvent identifier des objets plus petits qu’un fichier, y compris des objets incorporés dans un document composé, ou un pseudo-objet (comme une plage de cellules dans une feuille de calcul).

</dd> <dt>

<span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**Licensing**
</dt> <dd>

Fonctionnalité de COM qui permet de contrôler la création d’objets. Les objets sous licence ne peuvent être créés que par des clients autorisés à les utiliser. La gestion des licences est implémentée dans COM par le biais de l’interface [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) et par la prise en charge d’une clé de licence qui peut être transmise au moment de l’exécution.

</dd> <dt>

<span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**objet Link**
</dt> <dd>

Objet COM créé lors de la création ou du chargement d’un objet COM lié. L’objet Link est fourni par OLE et implémente l’interface [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) .

</dd> <dt>

<span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**objet lié**
</dt> <dd>

Objet COM dont les données sources résident physiquement là où elles ont été initialement créées. Seul un moniker qui représente les données sources et les données de présentation appropriées est conservé avec le document composé. Les modifications apportées à la source du lien sont automatiquement reflétées dans l’objet lié.

</dd> <dt>

<span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**lier la source**
</dt> <dd>

Données qui constituent la source d’un objet lié. Une source de lien peut être un fichier ou une partie d’un fichier, tel qu’une plage de cellules sélectionnée dans un fichier (également appelé Pseudo-objet).

</dd> <dt>

<span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**État chargé**
</dt> <dd>

L’état d’un objet après que ses structures de données ont été chargées en mémoire et sont accessibles au processus client.

</dd> <dt>

<span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**serveur local**
</dt> <dd>

Un serveur hors processus implémenté en tant qu’application .EXE s’exécutant sur le même ordinateur que son application cliente.

</dd> <dt>

<span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**Lock**
</dt> <dd>

Un pointeur s’est maintenu sur-et éventuellement, un nombre de références incrémenté sur un objet en cours d’exécution. OLE définit deux types de verrous qui peuvent être conservés sur un objet : fort et faible. Pour implémenter un verrou fort, un serveur doit conserver à la fois un pointeur et un décompte de références, afin que l’objet reste « verrouillé » en mémoire au moins jusqu’à ce que le serveur appelle [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Pour implémenter un verrou faible, le serveur gère uniquement un pointeur vers l’objet, afin que l’objet puisse être détruit par un autre processus.

</dd> <dt>

<span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**marshaling**
</dt> <dd>

Empaquetage et envoi d’appels de méthode d’interface à travers les limites de thread ou de processus.

</dd> <dt>

<span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**type de média**
</dt> <dd>

Extension de MIME qui autorise la négociation de format de données entre un client et un objet.

</dd> <dt>

<span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**Type de contenu MIME**
</dt> <dd>

Extension de MIME qui autorise la négociation de format de données entre un client et un objet.

</dd> <dt>

<span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**MIME (Multipurpose Internet Mail extension)**
</dt> <dd>

Protocole Internet développé à l’origine pour permettre l’échange de messages électroniques avec du contenu riche sur des environnements de réseau, d’ordinateur et de messagerie hétérogènes. En pratique, MIME a également été adopté et étendu par les applications non-messagerie.

</dd> <dt>

<span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**moniker**
</dt> <dd>

Objet qui implémente l’interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) . Un moniker agit comme un nom qui identifie de façon unique un objet COM. De la même façon qu’un chemin d’accès identifie un fichier dans le système de fichiers, un moniker identifie un objet COM dans l’espace de noms du répertoire.

</dd> <dt>

<span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**moniker (classe)**
</dt> <dd>

Implémentation de l’interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) . Les classes de moniker fournies par le système incluent les monikers de fichiers, les monikers d’élément, les monikers composites génériques, les anti-monikers, les monikers de pointeur et les monikers d’URL.

</dd> <dt>

<span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**client moniker**
</dt> <dd>

Application qui utilise des monikers pour obtenir des pointeurs d’interface vers des objets gérés par une autre application.

</dd> <dt>

<span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**fournisseur de moniker**
</dt> <dd>

Application qui rend les monikers disponibles qui identifient les objets qu’il gère, afin que les objets soient accessibles à d’autres applications.

</dd> <dt>

<span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**extension de l’espace de noms**
</dt> <dd>

Objet COM in-process qui implémente [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)et [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), qui sont parfois appelés interfaces d’extension d’espace de noms. Une extension d’espace de noms est utilisée pour étendre l’espace de noms de l’interpréteur de commandes ou pour créer un espace de noms distinct. les utilisateurs principaux sont l’explorateur de Windows et les boîtes de dialogue de fichier courantes.

</dd> <dt>

<span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**données natives**
</dt> <dd>

Données utilisées par une application serveur OLE lors de la modification d’un objet incorporé.

</dd> <dt>

<span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**dessin**
</dt> <dd>

Dans OLE, structure de programmation encapsulant à la fois les données et les fonctionnalités qui sont définies et allouées en tant qu’unité unique et pour lesquelles le seul accès public s’effectue via les interfaces de la structure de programmation. Un objet COM doit prendre en charge, au minimum, l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , qui maintient l’existence de l’objet pendant son utilisation et fournit l’accès aux autres interfaces de l’objet.

</dd> <dt>

<span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**État de l’objet** 
</dt> <dd>

Relation entre un objet de document composé dans son conteneur et l’application responsable de la création de l’objet : active, passive, chargée ou en cours d’exécution. Les objets passifs sont stockés sur le disque ou dans une base de données, et l’objet n’est pas sélectionné ou actif. Dans l’État chargé, les structures de données de l’objet ont été chargées en mémoire, mais elles ne sont pas disponibles pour les opérations telles que la modification. Les objets en cours d’exécution sont tous deux chargés et disponibles pour toutes les opérations. Les objets actifs exécutent des objets qui ont une interface utilisateur visible.

</dd> <dt>

<span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**nom du type d’objet**
</dt> <dd>

Chaîne d’identification unique stockée dans le cadre des informations disponibles pour un objet dans la base de données d’inscription.

</dd> <dt>

<span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**ActiveX**
</dt> <dd>

Technologie basée sur les objets de Microsoft permettant de partager des informations et des services au-delà des limites des processus et des ordinateurs.

</dd> <dt>

<span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**serveur hors processus**
</dt> <dd>

Un serveur, implémenté en tant qu’application .EXE, qui s’exécute en dehors du processus de son client, soit sur le même ordinateur, soit sur un ordinateur distant.

</dd> <dt>

<span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**paramètre de sortie**
</dt> <dd>

Un paramètre de sortie est alloué par la fonction appelée et libéré par l’appelant.

</dd> <dt>

<span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**état passif**
</dt> <dd>

État d’un objet COM lorsqu’il est stocké (sur disque ou dans une base de données). L’objet n’est pas sélectionné ou actif.

</dd> <dt>

<span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**propriété persistante**
</dt> <dd>

Informations qui peuvent être stockées de manière permanente dans le cadre d’un objet de stockage, tel qu’un fichier ou un répertoire. Les propriétés persistantes sont regroupées dans des jeux de propriétés, qui peuvent être affichés et modifiés.

Une propriété persistante est différente des propriétés d’exécution des objets créés avec les contrôles OLE et les technologies d’automatisation, qui peuvent être utilisées pour affecter le comportement du système. La structure [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) définit tous les types de propriétés persistantes valides, tandis que la structure **Variant** définit tous les types de propriétés d’exécution valides.

</dd> <dt>

<span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**stockage persistant**
</dt> <dd>

Stockage d’un fichier ou d’un objet dans un support, tel qu’un système de fichiers ou une base de données, afin que l’objet et ses données soient conservés lorsque le fichier est fermé, puis rouvert ultérieurement.

</dd> <dt>

<span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**image, objet**
</dt> <dd>

Objet COM qui fournit l’accès aux images GDI en implémentant l’interface [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) .

</dd> <dt>

<span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**moniker du pointeur**
</dt> <dd>

Moniker qui mappe un pointeur d’interface vers un objet en mémoire. Tandis que la plupart des monikers identifient les objets qui peuvent être stockés de manière permanente, les monikers de pointeur identifient les objets qui ne peuvent pas. Elles permettent à ces objets de participer à une opération de liaison de moniker.

</dd> <dt>

<span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**données de présentation**
</dt> <dd>

Données utilisées par un conteneur pour afficher des objets incorporés ou liés.

</dd> <dt>

<span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**verbe principal**
</dt> <dd>

Action associée aux opérations les plus courantes ou préférées effectuées par les utilisateurs sur un objet. Le verbe principal est toujours défini comme verbe zéro dans la base de données d’inscription du système. Le verbe principal d’un objet est exécuté en double-cliquant sur l’objet.

</dd> <dt>

<span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**propriété**
</dt> <dd>

Informations associées à un objet. Dans OLE, les propriétés se répartissent en deux catégories : les propriétés d’exécution et les propriétés persistantes. Les propriétés au moment de l’exécution sont généralement associées à des objets de contrôle ou à leurs conteneurs. Par exemple, la couleur d’arrière-plan est une propriété Runtime définie par le conteneur d’un contrôle. Les propriétés persistantes sont associées à des objets stockés.

</dd> <dt>

<span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**frame de propriété**
</dt> <dd>

Mécanisme d’interface utilisateur qui affiche une ou plusieurs pages de propriétés pour un contrôle. Le système d’exécution de contrôles OLE fournit une implémentation standard d’un frame de propriété qui est accessible à l’aide de la fonction d’assistance [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) .

</dd> <dt>

<span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**identificateur de propriété**
</dt> <dd>

Entier signé de 4 octets qui identifie une propriété persistante dans un jeu de propriétés.

</dd> <dt>

<span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**page de propriétés**
</dt> <dd>

Objet COM avec son propre CLSID qui fait partie d’une interface utilisateur, implémenté par un contrôle et qui permet d’afficher et de définir les propriétés du contrôle. Les objets page de propriétés implémentent l’interface [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) .

</dd> <dt>

<span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**site de la page de propriétés**
</dt> <dd>

Emplacement dans le frame d’une propriété où une page de propriétés est affichée. Le frame de propriété implémente l’interface [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) , qui contient des méthodes pour gérer les sites de chacune des pages de propriétés fournies par un contrôle.

</dd> <dt>

<span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**jeu de propriétés**
</dt> <dd>

Groupe de propriétés logiquement lié qui est associé à un objet stocké de manière permanente. Pour créer, ouvrir, supprimer ou énumérer un ou plusieurs jeux de propriétés, implémentez l’interface [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) . Si vous utilisez des fichiers composés, vous pouvez utiliser l’implémentation OLE de cette interface au lieu d’implémenter la vôtre.

</dd> <dt>

<span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**stockage des jeux de propriétés**
</dt> <dd>

Objet de stockage COM qui contient un jeu de propriétés. Un stockage de jeu de propriétés est un objet dépendant associé à et géré par un objet de stockage.

</dd> <dt>

<span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**feuille de propriétés**
</dt> <dd>

Ensemble de pages de propriétés pour un ou plusieurs objets.

</dd> <dt>

<span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**procur**
</dt> <dd>

Objet spécifique à l’interface qui conditionne les paramètres de cette interface en vue d’un appel de méthode distant. Un proxy s’exécute dans l’espace d’adressage de l’expéditeur et communique avec un stub correspondant dans l’espace d’adressage du destinataire.

</dd> <dt>

<span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**gestionnaire proxy**
</dt> <dd>

Dans le marshaling standard, proxy qui gère tous les proxies d’interface pour un objet unique.

</dd> <dt>

<span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**Pseudo-objet**
</dt> <dd>

Partie d’un document ou d’un objet incorporé, tel qu’une plage de cellules dans une feuille de calcul, qui peut être la source d’un objet COM.

</dd> <dt>

<span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**décompte de références**
</dt> <dd>

Le fait de conserver un décompte de chaque pointeur d’interface sur un objet pour s’assurer que l’objet n’est pas détruit avant que toutes les références à celui-ci ne soient libérées.

</dd> <dt>

<span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**moniker relatif**
</dt> <dd>

Moniker qui spécifie l’emplacement d’un objet par rapport à l’emplacement d’un autre objet. Un moniker relatif est analogue à un chemin d’accès relatif, tel que. \\ sauvegarder le \\ rapport. ancien.

</dd> <dt>

<span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**serveur distant**
</dt> <dd>

Une application serveur, implémentée en tant que fichier EXE, qui s’exécute sur un ordinateur différent de l’application cliente qui l’utilise.

</dd> <dt>

<span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**rétablir**
</dt> <dd>

Pour ignorer toutes les modifications apportées à un objet depuis la dernière validation des modifications ou l’ouverture du stockage de l’objet.

</dd> <dt>

<span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**objet de stockage racine**
</dt> <dd>

Objet de stockage le plus à l’extérieur dans un document. Un objet de stockage racine peut contenir d’autres objets de flux et de stockage imbriqués. Par exemple, un document composé est enregistré sur le disque sous la forme d’une série d’objets de stockage et de flux au sein d’un objet de stockage racine.

</dd> <dt>

<span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**État en cours d’exécution**
</dt> <dd>

État d’un objet COM lorsque son application serveur est en cours d’exécution et qu’il est possible d’accéder à ses interfaces et de recevoir des notifications de modifications.

</dd> <dt>

<span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**table ROT (Running Object Table)**
</dt> <dd>

Une table accessible globalement sur chaque ordinateur qui effectue le suivi de tous les objets COM dans l’État en cours d’exécution qui peuvent être identifiés par un moniker. Les fournisseurs de monikers inscrivent un objet dans la table, ce qui incrémente le décompte de références de l’objet. Pour que l’objet puisse être détruit, son moniker doit être libéré de la table.

</dd> <dt>

<span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**propriété au moment de l’exécution**
</dt> <dd>

Informations d’État discrètes associées à un objet de contrôle ou à son conteneur. Il existe trois types de propriétés d’exécution : les propriétés ambiantes, les propriétés de contrôle et les propriétés étendues.

</dd> <dt>

<span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**inscription automatique**
</dt> <dd>

Processus par lequel un serveur peut effectuer ses propres opérations de registre.

</dd> <dt>

<span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**application serveur**
</dt> <dd>

Application qui peut créer des objets COM. Les applications de conteneur peuvent ensuite incorporer ou lier ces objets.

</dd> <dt>

<span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**objet statique**
</dt> <dd>

Objet qui contient uniquement une présentation, sans données natives. Un conteneur peut traiter un objet statique comme s’il s’agissait d’un objet lié ou incorporé, à ceci près qu’il n’est pas possible de modifier un objet statique.

Un objet statique peut résulter, par exemple, de la rupture d’un lien sur un objet lié, c’est-à-dire que l’application serveur n’est pas disponible ou que l’utilisateur ne souhaite plus mettre à jour l’objet lié.

</dd> <dt>

<span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**objet de stockage**
</dt> <dd>

Objet COM qui implémente l’interface [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) . Un objet de stockage contient des objets de stockage imbriqués ou des objets de flux, ce qui donne l’équivalent d’une structure de répertoires/fichiers dans un seul fichier.

</dd> <dt>

<span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**objet de flux**
</dt> <dd>

Objet COM qui implémente l’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) . Un objet de flux est analogue à un fichier dans un répertoire ou un système de fichiers.

</dd> <dt>

<span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Stockage structuré**
</dt> <dd>

Technologie OLE permettant de stocker des fichiers composés dans des systèmes de fichiers natifs.

</dd> <dt>

<span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**talon**
</dt> <dd>

Quand les paramètres d’une fonction ou d’une méthode d’interface sont marshalés à travers une limite de processus, le stub est un objet spécifique à l’interface qui décompresse les paramètres marshalés et appelle la méthode requise. Le stub s’exécute dans l’espace d’adressage du destinataire et communique avec un proxy correspondant dans l’espace d’adressage de l’expéditeur.

</dd> <dt>

<span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**Gestionnaire de stub**
</dt> <dd>

Gère tous les stubs d’interface pour un seul objet.

</dd> <dt>

<span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**appel synchrone**
</dt> <dd>

Appel de fonction qui n’autorise pas l’exécution des instructions supplémentaires dans le processus appelant tant que la fonction n’est pas retournée.

</dd> <dt>

<span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**Registre système**
</dt> <dd>

référentiel à l’ensemble du système d’informations pris en charge par Windows, qui contient des informations sur le système et ses applications, y compris les clients et les serveurs OLE.

</dd> <dt>

<span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**mode d’accès transactionnel**
</dt> <dd>

Un des deux modes d’accès dans lesquels un objet de stockage peut être ouvert. Lorsqu’ils sont ouverts en mode traité, les modifications sont stockées dans des mémoires tampons jusqu’à ce que l’objet de stockage racine valide ses modifications.

</dd> <dt>

<span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**informations de type**
</dt> <dd>

Informations sur la classe d’un objet fournie par une bibliothèque de types. Pour fournir des informations de type, un objet COM implémente l’interface [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .

</dd> <dt>

<span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**transfert de données uniforme**
</dt> <dd>

Modèle pour le transfert de données via le presse-papiers, le glisser-déplacer ou l’automatisation. Les objets conformes à ce modèle implémentent l’interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) . Ce modèle remplace l’échange dynamique de données (DDE).

</dd> <dt>

<span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**unmarshaling**
</dt> <dd>

Décompression des paramètres qui ont été envoyés à un proxy au-delà des limites du processus.

</dd> <dt>

<span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**URL (Universal Resource Locator)**
</dt> <dd>

Identificateur utilisé par le World Wide Web pour les noms et les emplacements des objets sur Internet. OLE fournit une classe de moniker, un moniker d’URL, dont l’implémentation peut être utilisée pour lier un client aux objets identifiés par une URL.

</dd> <dt>

<span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**Moniker d’URL**
</dt> <dd>

Moniker basé sur une URL (Universal Resource Locator). Un client peut utiliser des monikers d’URL pour se lier aux objets qui résident sur Internet. La classe moniker d’URL fournie par le système prend en charge les liaisons synchrones et asynchrones.

</dd> </dl>

 

 