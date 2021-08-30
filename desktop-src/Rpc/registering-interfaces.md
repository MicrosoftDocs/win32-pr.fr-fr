---
title: Inscription des interfaces
description: Inscription d’une interface d’appel de procédure distante (RPC).
ms.assetid: c22e3fa8-98be-461a-b06d-292d3f655ffc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91a4a6b3c5762a2f9ae74aef5440a5be072f6686b795016df6e9324c240baea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018839"
---
# <a name="registering-interfaces"></a>Inscription des interfaces

Cette section présente en détail le processus d’inscription d’une interface RPC.

Les informations contenues dans cette section sont présentées dans les rubriques suivantes :

-   [Fonctions d’inscription de l’interface](#interface-registration-functions)
-   [Vecteurs de point d’entrée](#entry-point-vectors)
-   [EPVs Manager](#manager-epvs)
-   [Inscription d’une implémentation unique d’une interface](#registering-a-single-implementation-of-an-interface)
-   [Inscription de plusieurs implémentations d’une interface](#registering-multiple-implementations-of-an-interface)
-   [Règles d’appel des routines du gestionnaire](#rules-for-invoking-manager-routines)
-   [Distribution d’un appel de procédure distante à une routine Server-Manager](#dispatching-a-remote-procedure-call-to-a-server-manager-routine)
-   [Fournir votre propre fonction de Object-Inquiry](#supplying-your-own-object-inquiry-function)

## <a name="interface-registration-functions"></a>Fonctions d’inscription de l’interface

Les serveurs inscrivent leurs interfaces en appelant la fonction [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) . Les programmes serveur complexes prennent souvent en charge plusieurs interfaces. Les applications serveur doivent appeler cette fonction une fois pour chaque interface qu’elles prennent en charge.

En outre, les serveurs peuvent prendre en charge plusieurs versions de la même interface, chacune avec sa propre implémentation des fonctions de l’interface. Si votre programme serveur effectue cette opération, il doit fournir un ensemble de points d’entrée. Un point d’entrée est une routine Manager qui distribue les appels pour une version d’une interface. Il doit y avoir un point d’entrée pour chaque version de l’interface. Le groupe de points d’entrée est appelé vecteur de point d’entrée. Pour plus d’informations, consultez [vecteurs de point d’entrée](#entry-point-vectors).

En plus de la fonction standard [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), RPC prend également en charge d’autres fonctions d’inscription d’interface. La fonction [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) étend les fonctionnalités de **RpcServerRegisterIf** en vous permettant de spécifier un ensemble d’indicateurs d’inscription (voir [indicateurs d’inscription d’interface](interface-registration-flags.md)), le nombre maximal de demandes d’appel de procédure distante simultanées que le serveur peut accepter et la taille maximale en octets des blocs de données entrants.

La bibliothèque RPC contient également une fonction appelée [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex). À l’instar de la fonction [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) , cette fonction inscrit une interface. Votre programme serveur peut également utiliser cette fonction pour spécifier un ensemble d’indicateurs d’inscription (voir [indicateurs d’inscription](interface-registration-flags.md)de l’interface), le nombre maximal de demandes simultanées d’appel de procédure distante que le serveur peut accepter et une fonction de rappel de sécurité.

Les fonctions [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)et [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) définissent des valeurs dans la table de registre de l’interface interne. Cette table est utilisée pour mapper les UUID d’interface et d’objet à un EPV Manager. Le gestionnaire EPV est un tableau de pointeurs de fonction qui contient un seul pointeur de fonction pour chaque prototype de fonction dans l’interface spécifiée dans le fichier IDL.

Pour plus d’informations sur la fourniture de plusieurs EPVs pour fournir plusieurs implémentations de l’interface, consultez [plusieurs implémentations d’interface](#registering-multiple-implementations-of-an-interface).

La bibliothèque Runtime utilise la table de registre de l’interface (définie par les appels à la fonction [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)) et la table de registre des objets (définie par les appels à la fonction [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)) pour mapper les UUID d’interface et d’objet au pointeur de fonction.

Si vous souhaitez que votre programme serveur supprime une interface du registre de la bibliothèque Runtime RPC, appelez la fonction [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) . Une fois l’interface supprimée du Registre, la bibliothèque Runtime RPC n’accepte plus de nouveaux appels pour cette interface.

## <a name="entry-point-vectors"></a>Vecteurs de point d’entrée

Le vecteur de point d’entrée du gestionnaire (EPV) est un tableau de pointeurs de fonction qui pointent vers les implémentations des fonctions spécifiées dans le fichier IDL. Le nombre d’éléments dans le tableau correspond au nombre de fonctions spécifiées dans le fichier IDL. RPC prend en charge plusieurs vecteurs de point d’entrée représentant plusieurs implémentations des fonctions spécifiées dans l’interface.

Le compilateur MIDL génère automatiquement un type de données Manager EPV à utiliser lors de la création du gestionnaire EPVs. Le type de données est nommé * if-name ***\_ Server \_ EPV**, où *-Name* spécifie l’identificateur d’interface dans le fichier IDL.

Le compilateur MIDL crée et initialise automatiquement un EPV Manager par défaut en supposant qu’il existe une routine de gestion portant le même nom pour chaque procédure de l’interface et qu’elle est spécifiée dans le fichier IDL.

Lorsqu’un serveur offre plusieurs implémentations de la même interface, le serveur doit créer un EPV Manager supplémentaire pour chaque implémentation. Chaque EPV doit contenir exactement un point d’entrée (adresse d’une fonction) pour chaque procédure définie dans le fichier IDL. L’application serveur déclare et Initialise une variable Manager EPV de type *si-name * * * \_ Server \_ EPV** pour chaque implémentation supplémentaire de l’interface. Pour inscrire le EPVs, il appelle [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) une fois pour chaque type d’objet qu’il prend en charge.

Lorsque le client effectue un appel de procédure distante au serveur, le EPV contenant le pointeur de fonction est sélectionné en fonction de l’UUID de l’interface et du type d’objet. Le type d’objet est dérivé de l’UUID de l’objet par la fonction d’interrogation de l’objet ou le mappage piloté par la table contrôlé par [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype).

## <a name="manager-epvs"></a>EPVs Manager

Par défaut, le compilateur MIDL utilise les noms des procédures du fichier IDL d’une interface pour générer un EPV Manager, que le compilateur place directement dans le stub serveur. Ce EPV par défaut est initialisé de manière statique à l’aide des noms de procédure déclarés dans la définition de l’interface.

Pour inscrire un gestionnaire à l’aide de l’EPV par défaut, spécifiez **null** comme valeur du paramètre *MgrEpv* dans un appel à la fonction [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) . Si les noms de routine utilisés par un gestionnaire correspondent à ceux de la définition d’interface, vous pouvez inscrire ce gestionnaire à l’aide du EPV par défaut de l’interface générée par le compilateur MIDL. Vous pouvez également inscrire un gestionnaire à l’aide d’un EPV fourni par l’application serveur.

Un serveur peut (et parfois) créer et inscrire un EPV de gestionnaire non **null** pour une interface. Pour sélectionner un EPV fourni par l’application serveur, transmettez l’adresse d’un EPV dont la valeur a été déclarée par le serveur comme valeur de *MgrEpv* un paramètre. Une valeur non **null** pour le *MgrEpv* un paramètre remplace toujours un EPV par défaut dans le stub serveur.

Le compilateur MIDL génère automatiquement un type de données Manager EPV (RPC \_ Mgr \_ EPV) pour une application serveur à utiliser dans la création de EPVs Manager. Un EPV Manager doit contenir exactement un point d’entrée (adresse de fonction) pour chaque procédure définie dans le fichier IDL.

Un serveur doit fournir un EPV non **null** dans les cas suivants :

-   Lorsque les noms des routines du gestionnaire diffèrent des noms de procédure déclarés dans la définition de l’interface
-   Quand le serveur utilise le EPV par défaut pour inscrire une autre implémentation de l’interface

Un serveur déclare un gestionnaire EPV en initialisant une variable de type *si-name * * * \_ Server \_ EPV** pour chaque implémentation de l’interface.

## <a name="registering-a-single-implementation-of-an-interface"></a>Inscription d’une implémentation unique d’une interface

Lorsqu’un serveur n’offre qu’une seule implémentation d’une interface, le serveur appelle [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) une seule fois. Dans le cas standard, le serveur utilise le EPV Manager par défaut. (L’exception est lorsque le gestionnaire utilise des noms de routine qui diffèrent de ceux déclarés dans l’interface.)

Pour le cas standard, vous fournissez les valeurs suivantes pour les appels à [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2):

-   EPVs Manager

    Pour utiliser le EPV par défaut, spécifiez une valeur **null** pour le paramètre *MgrEpv* .

-   UUID du type de gestionnaire

    Lorsque vous utilisez le EPV par défaut, inscrivez l’interface avec un UUID de type gestionnaire Nil en fournissant une valeur **null** ou un UUID Nil pour *MgrTypeUuid* un paramètre. Dans ce cas, tous les appels de procédure distante, quel que soit l’UUID de l’objet dans leur handle de liaison, sont distribués au EPV par défaut, en supposant qu’aucun appel [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) n’ait été effectué.

    Vous pouvez également fournir un UUID de type gestionnaire non Nil. Dans ce cas, vous devez également appeler la routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) .

## <a name="registering-multiple-implementations-of-an-interface"></a>Inscription de plusieurs implémentations d’une interface

Vous pouvez fournir plusieurs implémentations de la ou des procédures distantes spécifiées dans le fichier IDL. L’application serveur appelle [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) pour mapper les UUID d’objet aux UUID de type et appelle [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) pour associer le gestionnaire EPVs à un UUID de type. Lorsqu’un appel de procédure distante arrive avec son UUID d’objet, la bibliothèque Runtime du serveur RPC mappe l’UUID de l’objet à un UUID de type. L’application serveur utilise ensuite le type UUID et l’UUID de l’interface pour sélectionner le EPV Manager.

Vous pouvez également spécifier votre propre fonction pour résoudre le mappage de l’UUID de l’objet à l’UUID du type de gestionnaire. Vous spécifiez la fonction de mappage lorsque vous appelez [**RpcObjectSetInqFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsetinqfn).

Pour offrir plusieurs implémentations d’une interface, un serveur doit inscrire chaque implémentation en appelant [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) séparément. Pour chaque implémentation qu’un serveur inscrit, il fournit le même *IfSpec* un paramètre, mais une autre paire de *MgrTypeUuid* et *MgrEpv* un paramètre.

Dans le cas de plusieurs gestionnaires, utilisez [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) comme suit :

-   EPVs Manager

    Pour offrir plusieurs implémentations d’une interface, un serveur doit :

    -   Créez un EPV de gestionnaire non **null** pour chaque implémentation supplémentaire.
    -   Spécifiez une valeur non **null** pour *MgrEpv* un paramètre dans [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2).

    Notez que le serveur peut également s’inscrire auprès du EPV Manager par défaut.

-   UUID du type de gestionnaire

    Fournissez un UUID de type de gestionnaire pour chaque EPV de l’interface. L’UUID du type Nil (ou la valeur **null** ) pour *MgrTypeUuid* un paramètre peut être spécifié pour l’un des EPVs Manager. Chaque UUID de type doit être différent.

## <a name="rules-for-invoking-manager-routines"></a>Règles d’appel des routines du gestionnaire

La bibliothèque Runtime RPC distribue un appel de procédure distante entrant à un responsable qui offre l’interface RPC demandée. Lorsque plusieurs gestionnaires sont inscrits pour une interface, la bibliothèque Runtime RPC doit en sélectionner une. Pour sélectionner un gestionnaire, la bibliothèque Runtime RPC utilise l’UUID d’objet spécifié par le handle de liaison de l’appel.

La bibliothèque Runtime applique les règles suivantes lors de l’interprétation de l’UUID de l’objet d’un appel de procédure distante :

-   UUID d’objets Nil

    L’UUID de type Nil est automatiquement affecté à un UUID d’objet Nil (il est illégal de spécifier un UUID d’objet Nil dans la routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) ). Par conséquent, un appel de procédure distante dont le handle de liaison contient un UUID d’objet Nil est automatiquement distribué au gestionnaire enregistré avec l’UUID de type Nil, le cas échéant.

-   UUID d’objets non Nil

    En principe, un appel de procédure distante dont le descripteur de liaison contient un UUID d’objet non Nil doit être traité par un gestionnaire dont le type UUID correspond au type de l’UUID de l’objet. Toutefois, l’identification du gestionnaire approprié nécessite que le serveur ait spécifié le type de cet UUID d’objet en appelant la routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) .

    Si un serveur ne parvient pas à appeler la routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) pour un UUID d’objet non Nil, un appel de procédure distante pour cet UUID d’objet accède au gestionnaire EPV qui sert les appels de procédure distante avec un UUID d’objet Nil (autrement dit, le type Nil UUID).

    Les appels de procédure distante avec un UUID d’objet non Nil dans le handle de liaison ne peuvent pas être exécutés si le serveur affecté à l’UUID d’un objet non Nil est un UUID de type en appelant la routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) , mais n’a pas également inscrit un EPV de gestionnaire pour ce type UUID en appelant [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2).

Le tableau suivant récapitule les actions que la bibliothèque Runtime utilise pour sélectionner la routine Manager.



| UUID d’objet de l’appel | Type de l’ensemble de serveurs pour l’UUID de l’objet ? | Type de EPV enregistré sur le serveur ? | Action de distribution                                                                                                                                 |
|---------------------|----------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Pli                 | Non applicable                   | Oui                         | Utilise le gestionnaire avec l’UUID de type Nil.                                                                                                           |
| Pli                 | Non applicable                   | No                          | Error ( \_ type RPC S \_ non pris en charge \_ ); rejette l’appel de procédure distante.                                                                              |
| Non Nil             | Oui                              | Oui                         | Utilise le gestionnaire avec le même UUID de type.                                                                                                          |
| Non Nil             | Non                                | Ignoré                     | Utilise le gestionnaire avec l’UUID de type Nil. S’il n’existe aucun gestionnaire avec l’UUID de type Nil, Error (RPC \_ S \_ UNSUPPORTEDTYPE); rejette l’appel de procédure distante. |
| Non Nil             | Oui                              | Non                          | Error (RPC \_ S \_ UNSUPPORTEDTYPE); rejette l’appel de procédure distante.                                                                                |



 

L’UUID d’objet de l’appel est l’UUID d’objet trouvé dans un handle de liaison pour un appel de procédure distante.

Le serveur définit le type de l’UUID de l’objet en appelant [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) pour spécifier l’UUID de type pour un objet.

Le serveur inscrit le type pour le EPV Manager en appelant [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) ou [**RPCSERVERREGISTERIF2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) en utilisant le même UUID de type.

> [!Note]  
> L’UUID de l’objet Nil reçoit toujours automatiquement l’UUID de type Nil. Il est interdit de spécifier un UUID d’objet Nil dans la routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) .

 

## <a name="dispatching-a-remote-procedure-call-to-a-server-manager-routine"></a>Distribution d’un appel de procédure distante à une routine de gestion de serveur

Les tableaux suivants présentent les étapes que prend la bibliothèque Runtime RPC pour distribuer un appel de procédure distante à une routine de gestionnaire de serveur.

Un cas simple où le serveur enregistre le EPV Manager par défaut, est décrit dans les tableaux suivants.

**Table de registre de l’interface**



| UUID de l’interface | UUID du type de gestionnaire | Vecteur de point d’entrée |
|----------------|-------------------|--------------------|
| *uuid1*        | Pli               | EPV par défaut        |



 

**Table de registre des objets**



| UUID de l’objet             | Type d’objet |
|-------------------------|-------------|
| Pli                     | Pli         |
| (Tout autre UUID d’objet) | Pli         |



 

**Mappage du handle de liaison à un vecteur de point d’entrée (EPV)**



| UUID de l’interface (à partir du handle de liaison client) | UUID d’objet (à partir du handle de liaison client) | Type d’objet (à partir de la table de registre des objets) | Manager EPV (à partir de la table de registre de l’interface) |
|---------------------------------------------|------------------------------------------|------------------------------------------|---------------------------------------------|
| *uuid1*                                     | Pli                                      | Pli                                      | EPV par défaut                                 |
| Identique à ce qui précède                               | *UUID*                                  | Pli                                      | EPV par défaut                                 |



 

Les étapes suivantes décrivent les actions que la bibliothèque Runtime du serveur RPC prend, comme indiqué dans les tableaux précédents, lorsqu’un client avec l’interface UUID *uuid1* l’appelle.

1.  Le serveur appelle [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) pour associer une interface qu’il propose avec l’UUID de type Manager Nil et avec le EPV du gestionnaire par défaut généré par MIDL. Cet appel ajoute une entrée dans la table de registre de l’interface. L’UUID de l’interface est contenu dans le paramètre *IfSpec* a.
2.  Par défaut, la table de registre des objets associe tous les UUID d’objets à l’UUID de type Nil. Dans cet exemple, le serveur n’appelle pas [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype).
3.  La bibliothèque Runtime du serveur reçoit un code de procédure distante contenant l’UUID de l’interface auquel appartient l’appel et l’UUID de l’objet à partir du handle de liaison de l’appel.

    Pour connaître la façon dont l’UUID d’un objet est défini dans un handle de liaison, consultez les entrées de référence de fonction suivantes :

    -   [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
    -   [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
    -   [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
    -   [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

4.  À l’aide de l’UUID de l’interface de l’appel de procédure distante, la bibliothèque Runtime du serveur localise cet UUID d’interface dans la table de registre de l’interface.

    Si le serveur n’a pas inscrit l’interface à l’aide de [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2), l’appel de procédure distante retourne à l’appelant avec un RPC \_ \_ Unknown \_ si le code d’État.

5.  À l’aide de l’UUID d’objet du handle de liaison, la bibliothèque Runtime du serveur localise cet UUID d’objet dans la table de registre des objets. Dans cet exemple, tous les UUID d’objets sont mappés au type d’objet Nil.
6.  La bibliothèque Runtime du serveur localise le type de gestionnaire Nil dans la table de registre de l’interface.
7.  La combinaison de l’UUID d’interface et du type Nil dans la table de registre de l’interface correspond à la valeur par défaut de EPV, qui contient les routines du gestionnaire de serveur à exécuter pour l’UUID d’interface figurant dans l’appel de procédure distante.

Supposons que le serveur offre plusieurs interfaces et plusieurs implémentations de chaque interface, comme décrit dans les tableaux suivants.

**Table de registre de l’interface**



| UUID de l’interface | UUID de type responsable | Vecteur de point d’entrée |
|----------------|-------------------|--------------------|
| *uuid1*        | Pli               | *epv1*             |
| *uuid1*        | *uuid3*           | *epv4*             |
| *uuid2*        | *uuid4*           | *epv2*             |
| *uuid2*        | *uuid7*           | *epv3*             |



 

**Table de registre des objets**



| UUID de l’objet      | Type d’objet |
|------------------|-------------|
| *UUID*          | *uuid3*     |
| *uuidB*          | *uuid7*     |
| *uuidC*          | *uuid7*     |
| *UUID*          | *uuid3*     |
| *UUID*          | *uuid3*     |
| *uuidF*          | *uuid8*     |
| Pli              | Pli         |
| (Tout autre UUID) | Pli         |



 

**Mappage du handle de liaison à un vecteur de point d’entrée**



| UUID de l’interface (à partir du handle de liaison client) | UUID d’objet (à partir du handle de liaison client) | Type d’objet (à partir de la table de registre des objets) | Manager EPV (à partir de la table de registre de l’interface) |
|---------------------------------------------|------------------------------------------|------------------------------------------|---------------------------------------------|
| *uuid1*                                     | Pli                                      | Pli                                      | *epv1*                                      |
| *uuid1*                                     | *UUID*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid1*                                     | *UUID*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid1*                                     | *UUID*                                  | *uuid3*                                  | *epv4*                                      |
| *uuid2*                                     | *uuidB*                                  | *uuid7*                                  | *epv3*                                      |
| *uuid2*                                     | *uuidC*                                  | *uuid7*                                  | *epv3*                                      |



 

Les étapes suivantes décrivent les actions effectuées par la bibliothèque Runtime du serveur, comme indiqué dans les tableaux précédents, lorsqu’un client avec l’interface UUID *uuid2* et l’UUID d’objet *uuidC* l’appelle.

1.  Le serveur appelle [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) pour associer les interfaces qu’il offre aux différents EPVs Manager. Les entrées de la table de registre de l’interface reflètent quatre appels de [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) pour offrir deux interfaces, avec deux implémentations (EPVs) pour chaque interface.
2.  Le serveur appelle [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) pour établir le type de chaque objet qu’il propose. En plus de l’Association par défaut de l’objet Nil à un type Nil, tous les autres UUID d’objets qui ne se trouvent pas explicitement dans la table de registre des objets sont également mappés à l’UUID de type Nil.

    Dans cet exemple, le serveur appelle la routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) six fois.

3.  La bibliothèque Runtime du serveur reçoit un appel de procédure distante contenant l’UUID d’interface auquel appartient l’appel et un UUID d’objet à partir du handle de liaison de l’appel.
4.  À l’aide de l’UUID de l’interface de l’appel de procédure distante, la bibliothèque Runtime du serveur localise l’UUID de l’interface dans la table de registre de l’interface.
5.  À l’aide de l’UUID de l’objet *uuidC* du handle de liaison, la bibliothèque Runtime du serveur localise l’UUID de l’objet dans la table de registre des objets et trouve qu’il est mappé au type *uuid7*.
6.  Pour localiser le type de gestionnaire, la bibliothèque Runtime du serveur combine l’UUID d’interface, *uuid2*, et le type *uuid7* dans la table de registre de l’interface. Cela correspond à *ePv3*, qui contient la routine du gestionnaire de serveur à exécuter pour l’appel de procédure distante.

Les routines dans *epv2* ne seront jamais exécutées, car le serveur n’a pas appelé la routine [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) pour ajouter des objets avec un UUID de type *uuid4* à la table de registre des objets.

Un appel de procédure distante avec l’interface UUID *uuid2* et l’UUID d’objet *uuidF* retourne à l’appelant avec un \_ code d’état de \_ type Mgr Unknown RPC, \_ \_ car le serveur n’a pas appelé [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif), [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)ou [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) pour inscrire l’interface avec un type de gestionnaire *uuid8*.

## <a name="return-values"></a>Valeurs de retour

Cette fonction retourne l’une des valeurs suivantes.



| Valeur                             | Signification                      |
|-----------------------------------|------------------------------|
| RPC \_ S \_ OK                        | Succès                      |
| \_type RPC \_ S \_ déjà \_ inscrit | UUID de type déjà inscrit |



 

## <a name="supplying-your-own-object-inquiry-function"></a>Fournir votre propre fonction de recherche d’objets

Imaginez un serveur qui gère des milliers d’objets de nombreux types différents. Chaque fois que le serveur a démarré, l’application serveur doit appeler la fonction [**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype) pour chacun des objets, même si les clients ne peuvent faire référence qu’à quelques-uns d’entre eux (ou prendre beaucoup de temps pour y faire référence). Ces milliers d’objets sont susceptibles d’être sur le disque, donc la récupération de leurs types prendrait beaucoup de temps. En outre, la table interne qui mappe l’UUID de l’objet à l’UUID du type de gestionnaire dupliquerait essentiellement le mappage géré avec les objets eux-mêmes.

Pour plus de commodité, l’ensemble de fonctions RPC comprend la fonction [**RpcObjectSetInqFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsetinqfn). Avec cette fonction, vous fournissez votre propre fonction d’interrogation d’objet.

Par exemple, vous pouvez fournir votre propre fonction de recherche d’objets lorsque vous mappez des objets 100 à 199 au type nombre 1, 200 – 299 au type numéro 2, et ainsi de suite. La fonction de recherche d’objets peut également être étendue à un système de fichiers distribués, où l’application serveur n’a pas de liste de tous les fichiers (UUID d’objets) disponibles, ou lorsque les UUID d’objet nomment les fichiers dans le système de fichiers et que vous ne souhaitez pas précharger tous les mappages entre les UUID d’objet et les UUID de type.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
</dt> <dt>

[**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)
</dt> <dt>

[**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)
</dt> <dt>

[**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[**RpcObjectSetType**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcobjectsettype)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 




