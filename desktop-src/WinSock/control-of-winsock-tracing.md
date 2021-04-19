---
description: .
ms.assetid: b079bdfc-b192-451c-967d-dcefa94b7ec7
title: Contrôle du suivi Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910b15ece4581525fddc25213c630e24d0e49110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514610"
---
# <a name="control-of-winsock-tracing"></a>Contrôle du suivi Winsock

Le suivi Winsock peut être contrôlé à l’aide de l’une des méthodes suivantes :

-   Outils de ligne de commande

    Deux outils en ligne de commande sont inclus avec Windows Vista et Windows Server 2008 qui sont utilisés pour contrôler le suivi et convertir le fichier journal de suivi binaire en texte lisible.

    L’outil **logman.exe** est utilisé pour démarrer ou arrêter le suivi Winsock.

    L’outil **tracerpt.exe** est utilisé pour convertir le fichier journal de suivi binaire en fichier texte lisible.

-   Observateur d'événements

    Le observateur d’événements sur Windows Vista et versions ultérieures peut également être utilisé pour activer le suivi Winsock. Le observateur d’événements est accessible sous outils d’administration à partir du menu Démarrer.

## <a name="using-logman-and-tracert"></a>Utilisation de logman et de tracert

Le suivi d’événements réseau Winsock est désactivé par défaut sur Windows Vista et versions ultérieures.

La commande suivante démarre le suivi d’événements réseau Winsock sur un ordinateur, définit le nom de la session de suivi d’événements sur mywinsocksession et envoie la sortie vers un fichier journal binaire appelé winsocklogfile. ETL :

**logman start-ETS mywinsocksession-o winsocklogfile. etl-p Microsoft-Windows-Winsock-AFD**

Les fichiers journaux sont créés dans le répertoire actif avec des noms de fichiers au format winsocklogfile \_ 000001. etl

La commande suivante arrête le suivi Winsock ci-dessus sur un ordinateur pour la session nommée mywinsocksession :

**logman stop-ETS mywinsocksession**

Un fichier journal binaire sera écrit à l’emplacement spécifié par le paramètre – o. Pour convertir le fichier binaire en fichier texte lisible, **tracerpt.exe** est utilisé :

**tracerpt.exe <nom du fichier. etl> – o winsocktracelog.txt**

Si un fichier de sortie contenant du code XML plutôt que du texte brut est préféré, la commande suivante est utilisée :

**tracerpt.exe <nom du fichier. etl> – o winsocktracelog.xml – XML**

Le suivi des modifications du catalogue Winsock est activé par défaut sur Windows Vista et versions ultérieures.

> [!Note]  
> Les fournisseurs de services en couche sont déconseillés. À compter de Windows 8 et de Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).

 

La commande suivante démarre le suivi des modifications du catalogue Winsock pour les fournisseurs de services en couche (LSP) sur un ordinateur, définit le nom de la session de suivi d’événements sur mywinsockcatalogsession et envoie la sortie vers un fichier journal binaire appelé winsockcataloglogfile. ETL :

**logman start-ETS mywinsockcatalogsession-o winsockcataloglogfile. etl-p Microsoft-Windows-Winsock-WS2HELP**

Les fichiers journaux sont créés dans le répertoire actif avec des noms de fichiers au format winsockcataloglogfile \_ 000001. etl

La commande suivante arrête le suivi Winsock ci-dessus sur un ordinateur pour la session nommée MySession :

**logman stop-ETS mywinsockcatalogsession**

Un fichier journal binaire sera écrit à l’emplacement spécifié par le paramètre – o. Pour convertir le fichier binaire en fichier texte lisible, **tracerpt.exe** est utilisé :

**tracerpt.exe <nom du fichier. etl> – o winsockcatalogtracelog.txt**

Si un fichier de sortie contenant du code XML plutôt que du texte brut est préféré, la commande suivante est utilisée :

**tracerpt.exe <nom du fichier. etl> – o winsockcatalogtracelog.xml – XML**

## <a name="using-event-viewer-to-start-winsock-network-event-tracing"></a>Utilisation de observateur d’événements pour démarrer le suivi d’événements réseau Winsock

Lorsque vous ouvrez observateur d’événements, le volet gauche contient la liste des événements. Ouvrez **journaux des applications et des services** , accédez à **\\ \\ événement réseau Microsoft Windows Winsock** comme source et sélectionnez **opérationnel**.

Dans le volet action, sélectionnez **Propriétés du journal** , puis activez la case à cocher **activer la journalisation** . Une fois la journalisation activée, vous pouvez également modifier la taille du fichier journal si nécessaire.

Le suivi d’événements réseau Winsock est maintenant activé et il vous suffit de cliquer sur l’action Actualiser pour mettre à jour la liste des événements qui ont été journalisés. Pour arrêter la journalisation, décochez simplement la case d’option.

Vous devrez peut-être augmenter la taille du journal en fonction du nombre d’événements que vous souhaitez afficher. L’un des inconvénients de l’utilisation de la observateur d’événements pour le suivi Winsock est qu’elle ne charge pas toutes les ressources de type chaîne, de sorte que les messages affichés dans le champ Description (une fois que vous sélectionnez un événement) sont parfois difficiles à lire (un argument qui doit être au format hexadécimal s’affiche au format décimal, par exemple). Toutefois, vous pouvez sélectionner l’onglet **Détails** dans la description de l’événement qui affiche l’entrée de journal XML brute qui a généralement plus de compréhension des arguments.

## <a name="using-event-viewer-to-start-winsock-catalog-change-tracing"></a>Utilisation de observateur d’événements pour démarrer le suivi des modifications du catalogue Winsock

Lorsque vous ouvrez observateur d’événements, le volet gauche contient la liste des événements. Ouvrez **journaux des applications et des services** , puis accédez à **Microsoft \\ Windows \\ Winsock Catalog change** comme source et sélectionnez **Operational (opérationnel**).

Dans le volet action, sélectionnez **Propriétés du journal** , puis activez la case à cocher **activer la journalisation** . Une fois la journalisation activée, vous pouvez également modifier la taille du fichier journal si nécessaire.

Le suivi des modifications du catalogue Winsock est maintenant activé et il vous suffit de cliquer sur l’action Actualiser pour mettre à jour la liste des événements qui ont été journalisés. Pour arrêter la journalisation, décochez simplement la case d’option.

Vous devrez peut-être augmenter la taille du journal en fonction du nombre d’événements que vous souhaitez afficher. L’un des inconvénients de l’utilisation de la observateur d’événements pour le suivi Winsock est qu’elle ne charge pas toutes les ressources de type chaîne, de sorte que les messages affichés dans le champ Description (une fois que vous sélectionnez un événement) sont parfois difficiles à lire (un argument qui doit être au format hexadécimal s’affiche au format décimal, par exemple). Toutefois, vous pouvez sélectionner l’onglet **Détails** dans la description de l’événement qui affiche l’entrée de journal XML brute qui a généralement plus de compréhension des arguments.

## <a name="interpreting-winsock-tracing-logs"></a>Interprétation des journaux de suivi Winsock

Tous les événements de suivi Winsock d’un journal contiennent deux types d’informations :

-   Système
-   EventData

Les informations système contiennent le niveau de journalisation, l’heure à laquelle l’entrée de journal a été créée, l’ID d’événement qui représente le type d’événement, l’ID de processus d’exécution, l’ID de thread d’exécution et d’autres informations système. Un niveau de journal de 4 dans le suivi Winsock représente la journalisation des événements d’informations. Un niveau de journal de 5 dans le suivi Winsock représente la journalisation des événements détaillé.

L’ID de processus d’exécution et l’ID de thread dans les informations système indiquent le processus et le thread qui étaient en cours d’exécution lorsque l’événement s’est produit. Dans de nombreux cas, cela représente un thread et un processus de noyau ou de travail, et non un thread en mode utilisateur, ni le processus de l’application. Ce champ n’est donc généralement pas très utile.

Chaque type d’événement de suivi Winsock a un ID d’événement unique dans la section système des données journalisées. Ces ID d’événement peuvent facilement être utilisés pour filtrer un fichier journal pour des événements de suivi Winsock spécifiques.

EVENTDATA contient des informations spécifiques au type d’événement.

Le paramètre Process dans les informations EventData est l’adresse de la structure EPROCESS du noyau pour le processus, et non le PID réel. Pour faire correspondre un événement au PID du mode utilisateur, prenez la valeur process des informations EventData à partir de n’importe quelle entrée de journal et recherchez un événement de création de socket avec la valeur de processus plus haut dans le journal. Une fois qu’une correspondance est trouvée, le dernier paramètre dans les données d’événement de création de socket est l’ID de processus en mode utilisateur qui a créé le Socket.

Un paramètre d’adresse dans les informations EventData est retourné dans certains événements de suivi Winsock. Un paramètre d’adresse représente une adresse IP, mais il est affiché dans le fichier texte créé par l’outil **tracerpt.exe** ou dans observateur d’événements en tant qu’octets bruts ou nombre. Les adresses IPv6 sont affichées au format hexadécimal et sont donc plus faciles à comprendre. Les adresses IPv4 sont affichées sous la forme d’un grand nombre décimal. Les développeurs doivent convertir manuellement les octets bruts d’une adresse IPv4 en notation d’adresse décimale décimale en points plus familière pour mieux pouvoir interpréter la valeur.

Un paramètre d’erreur dans EventData est retourné dans certains événements de suivi Winsock. Un paramètre d’erreur se présente sous la forme d’un code d’erreur NTSTATUS ou HRESULT. Ce paramètre d’erreur s’affiche dans le fichier texte créé par l’outil **tracerpt.exe** ou dans observateur d’événements sous la forme d’un nombre décimal. Les développeurs doivent convertir manuellement le nombre décimal en nombre hexadécimal afin de mieux interpréter le code d’erreur dans certains cas.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Suivi Winsock](winsock-tracing.md)
</dt> <dt>

[Détails du suivi de modification du catalogue Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Détails du suivi d’événements réseau Winsock](winsock-tracing-event-details.md)
</dt> <dt>

[Niveaux de suivi Winsock](winsock-tracing-levels.md)
</dt> </dl>

 

 
