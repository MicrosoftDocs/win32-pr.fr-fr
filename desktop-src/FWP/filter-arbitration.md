---
title: Arbitrage de filtre
description: l’arbitrage de filtre est la logique intégrée à la plate-forme de filtrage Windows (WFP) qui est utilisée pour déterminer comment les filtres interagissent entre eux lors de la prise de décisions de filtrage du trafic réseau.
ms.assetid: d097f307-113e-4dc3-ad59-ddfb85061583
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7640e94440cf040d9ca51b6c639dc66e3e8a767024d6dbcd01b9c0cd2b87a24b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151186"
---
# <a name="filter-arbitration"></a>Arbitrage de filtre

l’arbitrage de filtre est la logique intégrée à la plate-forme de filtrage Windows (WFP) qui est utilisée pour déterminer comment les filtres interagissent entre eux lors de la prise de décisions de filtrage du trafic réseau.

## <a name="filter-arbitration-behaviors"></a>Comportements d’arbitrage de filtre

Les comportements suivants caractérisent le système d’arbitrage de filtre :

-   Tout le trafic peut être inspecté. Aucun trafic ne peut contourner des filtres au niveau d’une couche donnée.
-   Le trafic peut être bloqué par un filtre de légende via un **veto** , même si un filtre de priorité plus élevé l’a autorisé.
-   Plusieurs fournisseurs peuvent inspecter le trafic au niveau de la même couche. Par exemple, un pare-feu suivi de filtres d’identification (IDS) de système de détection d’intrusion ou IPsec, suivis de la qualité de service (QoS), peut examiner le trafic au niveau de la même couche.

## <a name="filtering-model"></a>Modèle de filtrage

Chaque couche de filtre est divisée en sous-couches classées par priorité (également appelées pondération). Le trafic réseau parcourt les sous-couches de la priorité la plus élevée à la priorité la plus basse. Les sous-couches sont créées et gérées par les développeurs à l’aide de l’API WFP.

Dans chaque sous-couche, les filtres sont classés par poids. Le trafic réseau est indiqué pour faire correspondre les filtres du poids le plus élevé au poids le plus bas.

L’algorithme d’arbitrage de filtre est appliqué à toutes les sous-couches d’une couche et la décision de filtrage finale est prise après l’évaluation de toutes les sous-couches. Cela fournit une capacité de correspondance multiple.

Dans une sous-couche, l’arbitrage de filtre est exécuté comme suit :

-   Calculez la liste des filtres correspondants classés par ordre décroissant, du plus élevé au plus bas.
-   Évaluer les filtres correspondants dans l’ordre jusqu’à ce qu’un « autoriser » ou un « bloc » soit renvoyé (les filtres peuvent également retourner « continuer ») ou jusqu’à épuisement de la liste.
-   Ignore les filtres restants et retourne l’action à partir du dernier filtre évalué.

Dans une couche, l’arbitrage de filtre est exécuté comme suit :

-   Effectuez un arbitrage de filtre à chaque sous-couche, dans l’ordre, de la priorité la plus basse à la priorité la plus basse.
-   Évaluer toutes les sous-couches même si une sous-couche de priorité supérieure a décidé de bloquer le trafic.
-   Retournez l’action résultante en fonction des règles de stratégie décrites dans la section suivante.

Le diagramme ci-dessous illustre un exemple de configuration de sous-couche. Les zones externes représentent des couches. Les zones internes représentent des sous-couches qui contiennent des filtres. Le caractère générique ( \* ) dans un filtre signifie que tout le trafic correspond au filtre.

![exemple de configuration de la sous-couche](images/fwp-sub-config2.png)

La seule façon d’ignorer un filtre est qu’un filtre de poids supérieur a autorisé ou bloqué le trafic au sein de la même sous-couche. À l’inverse, pour s’assurer qu’un filtre voit toujours tout le trafic au sein d’une couche, vous pouvez ajouter une sous-couche qui contient un filtre unique qui correspond à tout le trafic.

## <a name="configurable-override-policy"></a>Stratégie de remplacement configurable

Les règles décrites ci-dessous régissent les décisions d’arbitrage au sein d’une couche. Ces règles sont utilisées par le moteur de filtre pour décider de l’une des actions de sous-couche qui est appliquée au trafic réseau.

La stratégie de base est la suivante.

-   Les actions sont évaluées dans l’ordre de priorité des sous-couches, de la priorité la plus élevée à la priorité la plus basse.
-   « Block » remplace « permit ».
-   « Block » est final (ne peut pas être substitué) et arrête l’évaluation. Le paquet est rejeté.

La stratégie de base ne prend pas en charge le scénario d’une exception qui n’est pas remplacée par un pare-feu. Voici quelques exemples typiques de ce type de scénario :

-   Le port d’administration à distance doit être ouvert même en présence d’un pare-feu tiers.
-   Les composants qui requièrent l’ouverture de ports pour fonctionner (par exemple, Universal Plug-and-Play UPnP). Si l’administrateur a explicitement activé le composant, le pare-feu ne doit pas bloquer le trafic en mode silencieux.

Afin de prendre en charge les scénarios ci-dessus, une décision de filtrage doit être rendue plus difficile à remplacer qu’une autre décision de filtrage en gérant l’autorisation de remplacement d’action. Cette autorisation est implémentée en tant qu’indicateur d' **\_ écriture d' \_ action \_ FWPS Right** et est définie pour chaque filtre.

L’algorithme d’évaluation gère l’action en cours (« autoriser » ou « bloquer »), ainsi que l’indicateur d' **\_ écriture d' \_ action \_ FWPS à droite** . L’indicateur détermine si une sous-couche de priorité inférieure est autorisée à remplacer l’action. En définissant ou en réinitialisant l’indicateur d' **\_ écriture d' \_ action \_ FWPS à droite** dans la structure [FWPS \_ classifier \_ OUT0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_classify_out0) , un fournisseur régit la façon dont les actions peuvent ou ne peuvent pas être remplacées. Si l’indicateur est défini, il indique que l’action peut être substituée. Si l’indicateur est absent, l’action ne peut pas être substituée.



| Action | Autoriser le remplacement (l' \_ écriture d’action FWPS Right \_ \_ est définie) | Description                                                                                                          |
|--------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Permit | Oui                                                | Le trafic peut être bloqué sur une autre sous-couche. C’est ce qu’on appelle une autorisation souple.<br/>                            |
| Permit | Non                                                 | Le trafic peut être bloqué sur une autre sous-couche uniquement par un **refus** de la légende. C’est ce qu’on appelle une autorisation dure.<br/> |
| Bloquer  | Oui                                                | Le trafic peut être autorisé sur une autre sous-couche. C’est ce qu’on appelle un bloc souple.<br/>                           |
| Bloquer  | Non                                                 | Le trafic ne peut pas être autorisé sur une autre sous-couche. C’est ce qu’on appelle un bloc Hard.<br/>                        |



 

L’action de filtre peut être définie en définissant le membre de **type** dans la structure [**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0) sur le **\_ \_ bloc d’action fwp** ou l' **\_ \_ autorisation d’action fwp**. En même temps que le type d’action, un filtre expose également l’indicateur de filtre FWPM indicateur de l' **\_ \_ \_ \_ action effacer \_ le droit**. Si cet indicateur est désactivé, le type d’action est difficile et ne peut pas être substitué, sauf lorsqu’une autorisation dure est remplacée par un **veto** comme expliqué plus tard, sinon il est soft qui peut être remplacé par une action de haute priorité.

Le tableau suivant répertorie le comportement par défaut pour les actions de filtre et de légende.

| Action         | Comportement par défaut |
|----------------|------------------|
| Autorisation de filtre  | Autorisation souple      |
| Autorisation de la légende | Autorisation souple      |
| Filtrer le bloc   | Bloc matériel       |
| Bloc de légende  | Bloc souple       |



 

Un **veto** est une action « bloquer » renvoyée par le filtre lorsque l’indicateur d' **\_ écriture d' \_ action \_ FWPS à droite** a été réinitialisé avant d’appeler le filtre. Un **veto** bloquera le trafic autorisé avec une autorisation matérielle.

Lorsqu’un **veto** est émis, il s’agit d’une indication de conflit dans la configuration. Les actions suivantes sont prises pour atténuer le conflit.

-   Le trafic est bloqué.
-   Un événement d’audit est généré.
-   Une notification est générée.
    > [!Note]  
    > La notification est reçue par toutes les entités qui y sont abonnés. Cela inclut généralement le pare-feu (afin de détecter les mal-configurations) ou les applications (afin de détecter si leur filtre particulier est remplacé).

     

    > [!Note]  
    > Aucune interface utilisateur (IU) obligatoire n’est instanciée lorsqu’un filtre d’autorisation dure est substitué. Les notifications du remplacement sont envoyées à n’importe quel fournisseur inscrit pour les recevoir, ce qui permet aux pare-feu ou aux applications qui ont créé les filtres d’autorisation d’afficher l’interface utilisateur qui demande l’action de l’utilisateur. Il n’y a aucune valeur dans la notification de l’interface utilisateur de la plateforme pour ces événements de remplacement, car les éditeurs de logiciels indépendants qui ne veulent pas bloquer de manière silencieuse peuvent le faire en s’inscrivant à un emplacement différent dans WFP, ou (moins privilégié) gérer toute leur logique dans un pilote d’appel sortant. Les éditeurs de logiciels indépendants (ISV) qui envisagent d’inviter les utilisateurs sont d’une bonne idée de posséder l’expérience utilisateur et de créer leur propre interface utilisateur.

     

Le comportement d’atténuation décrit ci-dessus permet de s’assurer qu’un filtre d’autorisation « dure » n’est pas silencieusement remplacé par un filtre « bloquer » et qu’il couvre le scénario dans lequel un port d’administration à distance n’est pas autorisé à être bloqué par le pare-feu. Afin de remplacer silencieusement les filtres de « disque dur », un pare-feu doit ajouter ses filtres dans une sous-couche de priorité supérieure.

> [!Note]  
> Étant donné qu’il n’y a pas d’arbitrage inter-couche, le trafic autorisé avec « autorisation matérielle » peut toujours être bloqué sur une autre couche. Il incombe à l’auteur de la stratégie de s’assurer que le trafic est autorisé au niveau de chaque couche, si nécessaire.

 

Les applications utilisateur qui demandent des ports à ouvrir ajoutent des filtres remplaçables à une sous-couche basse priorité. Le pare-feu peut s’abonner au filtre ajouter des événements de notification et ajouter un filtre correspondant après la validation de l’utilisateur (ou de la stratégie).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Affectation de poids de filtre](filter-weight-assignment.md)
</dt> </dl>

 

