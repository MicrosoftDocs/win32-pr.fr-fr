---
title: Création de reconcilers de porte-documents
description: Un réconciliateur de porte-documents permet de rapprocher les différentes versions d’un document.
ms.assetid: 86d66291-96ae-40ea-98ef-ef263f25aa82
keywords:
- réconciliations de porte-documents
- rapprochement
- IReconcilableObject
- IReconcileInitiator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4161796999172e6ee9bc7c403e723f9f8bafe7e876b544888fa5e7105b724f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119556939"
---
# <a name="creating-briefcase-reconcilers"></a>Création de reconcilers de porte-documents

Un réconciliateur de porte-documents permet de rapprocher les différentes versions d’un document.

-   [À propos des réconciliateurs de porte-documents](#about-briefcase-reconcilers)
    -   [Rapprochement](#reconciliation)
    -   [Création d’un réconciliateur de porte-documents](#creating-a-briefcase-reconciler)
    -   [Interaction de l’utilisateur dans le rapprochement](#user-interaction-in-reconciliation)
    -   [Rapprochement des objets incorporés](#reconciling-embedded-objects)
    -   [Résidus](#residues)
-   [Référence du réconciliateur de porte-documents](#briefcase-reconciler-reference)
    -   [Méthodes et interfaces du réconciliateur de porte-documents](#briefcase-reconciler-interfaces-and-methods)

## <a name="about-briefcase-reconcilers"></a>À propos des réconciliateurs de porte-documents

Un réconciliateur de porte-documents associe différentes versions d’entrée d’un document pour produire une nouvelle version de sortie unique du document. Vous devrez peut-être créer un réconciliateur de porte-documents pour prendre en charge votre type de document. Cette vue d’ensemble décrit les réconcilieurs de porte-documents et explique comment les créer.

Les rubriques suivantes sont présentées :

-   [Rapprochement](#reconciliation)
-   [Création d’un réconciliateur de porte-documents](#creating-a-briefcase-reconciler)
-   [Interaction de l’utilisateur dans le rapprochement](#user-interaction-in-reconciliation)
-   [Rapprochement des objets incorporés](#reconciling-embedded-objects)
-   [Résidus](#residues)

### <a name="reconciliation"></a>Rapprochement

Un document est une collection d’informations qui peuvent être copiées et modifiées. Un document a des versions différentes si le contenu d’au moins deux copies du document est différent. Le rapprochement produit une seule version d’un document à partir de deux ou de plusieurs versions initiales. En règle générale, la version conciliée est une combinaison d’informations des versions initiales avec les informations les plus récentes ou les plus utiles préservées.

Le rapprochement est initié par le porte-documents lorsqu’il détermine que deux ou plusieurs copies du même document sont différentes. Le porte-documents, qui joue le rôle d’initiateur dans ce contexte, localise et démarre le réconciliateur de porte-documents associé au type de document donné. Le réconciliateur compare les documents et détermine les portions de documents à conserver. Certains réconcilieurs peuvent nécessiter une interaction de l’utilisateur pour terminer le rapprochement. D’autres peuvent terminer la conciliation sans intervention de l’utilisateur. Le réconcilieur peut être contenu dans une application ou être une extension implémentée en tant que DLL.

Certains réconcilieurs de porte-documents peuvent créer des résidus. Un résidu est un document, qui a généralement le même type de fichier que le document initial, qui contient des informations non enregistrées dans la version fusionnée. Les résidus sont généralement utilisés pour fournir aux auteurs un moyen rapide de déterminer les informations de leur document d’origine ne se trouvant pas dans la version fusionnée finale. Si un réconciliateur prend en charge les résidus, il crée un résidu pour chacune des versions d’origine du document. Les résidus ne sont pas créés, sauf si l’initiateur les demande.

Certaines réconciliations de porte-documents fonctionnent avec le porte-documents pour permettre à l’utilisateur de terminer la conciliation. Il s’agit d’une fonctionnalité importante pour un utilisateur qui peut décider que le rapprochement ne doit pas continuer. Un réconciliateur fournit généralement un objet d’arrêt lorsque le rapprochement requiert une intervention de l’utilisateur et peut être long. Dans certains environnements, un réconciliateur peut autoriser un rapprochement partiel, ce qui permet à un utilisateur d’interrompre temporairement un rapprochement et de le reprendre ultérieurement. Toutefois, le porte-documents ne prend pas en charge actuellement la conciliation partielle.

### <a name="creating-a-briefcase-reconciler"></a>Création d’un réconciliateur de porte-documents

Vous créez un réconciliateur de porte-documents en implémentant les interfaces de réconciliation. Au minimum, un réconciliateur implémente l’interface [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) et l’interface [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) ou [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) . En tant qu’initiateur, le porte-documents détermine le moment où le rapprochement est nécessaire et appelle la méthode [**IReconcilableObject :: Reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) pour initier le rapprochement.

Bien que [**IReconcilableObject :: Reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) offre un ensemble vaste de fonctionnalités de rapprochement, un réconciliateur de porte-documents n’effectue qu’une réconciliation minimale dans la plupart des cas. En particulier, le porte-documents ne nécessite pas que le réconciliateur prenne en charge la génération de résidus ou prenne en charge l’objet d’arrêt. En outre, le réconciliateur effectue une seule réconciliation de haut en bas et ne doit pas retourner la \_ valeur Rec E \_ NOTCOMPLETE ; autrement dit, il ne doit pas essayer le rapprochement partiel.

Le porte-documents fournit l’interface [**IReconcileInitiator**](ireconcileinitiator.md) . Le réconciliateur de porte-documents peut utiliser la méthode [**IReconcileInitiator :: SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback) pour définir l’objet d’arrêt. Le porte-documents n’utilise pas les identificateurs de version et ne peut donc pas fournir de versions antérieures d’un document si un réconciliateur les demande à l’aide des méthodes correspondantes dans **IReconcileInitiator**.

Le porte-documents passe à [**IReconcilableObject :: rapprocher**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) les monikers de fichiers représentant les versions du document à rapprocher. Le réconciliateur de porte-documents accède à la version à l’aide de la méthode [IMoniker :: BindToObject](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) ou [IMoniker :: BindToStorage](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) . Ce dernier est généralement plus rapide et recommandé. Le réconciliateur doit libérer tout objet ou stockage auquel il est lié.

Lorsque le réconciliateur de porte-documents utilise [IMoniker :: BindToStorage](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage), il se lie au stockage plat (un flux) ou à un stockage structuré OLE. Si le réconciliateur attend un stockage plat, il doit utiliser IMoniker :: BindToStorage pour demander l’interface [IStream](/windows/win32/api/objidl/nn-objidl-istream) . Si le réconciliateur attend un stockage structuré, il doit demander l’interface [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) . Dans les deux cas, il doit demander un accès direct en lecture seule (non-Transact) au stockage. l’accès en lecture/écriture n’est peut-être pas disponible.

Un réconciliateur de porte-documents minimal examine généralement directement le stockage des autres versions et traite les objets incorporés de manière très primitive, tels que la fusion de deux versions de l’objet en incluant les deux versions dans la version de sortie.

L’initiateur localise le réconciliateur de porte-documents approprié en utilisant un sous-ensemble de la logique implémentée par la fonction [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile) pour déterminer le type d’un fichier donné, puis recherche dans le registre la classe de réconciliateur associée au type de fichier donné. Le porte-documents, comme les autres composants de Shell, détermine le type d’un fichier uniquement par l’extension de nom de fichier. L’extension d’un fichier doit avoir un type de fichier inscrit pour que le porte-documents appelle un réconciliateur pour le fichier. Vous devez définir une entrée de Registre au format suivant lors de l’installation de votre réconciliateur.

```
CLSID
   {the file CLSID}
      Roles
         Reconciler
            (Default) = {the reconciler-classid}
```

La classe doit être à chargement rapide, doit être désignée \_ MULTIPLEUSE et, à moins que des marshaleurs ne soient fournis pour l’interface de réconciliation, doive être un serveur in-process (contenu dans une dll) plutôt qu’un serveur local (implémenté dans un fichier .exe).

### <a name="user-interaction-in-reconciliation"></a>Interaction de l’utilisateur dans le rapprochement

Un réconciliateur de porte-documents doit tenter d’effectuer une réconciliation sans intervention de l’utilisateur. Plus la réconciliation est automatisée, plus la perception de l’utilisateur du processus est bonne.

Dans certains cas, l’intervention de l’utilisateur peut être utile. Par exemple, un système de documents peut demander à un utilisateur de réviser les modifications avant d’accepter la version fusionnée d’un document ou peut nécessiter des commentaires de la part de l’utilisateur expliquant les modifications apportées. Dans ce cas, l’initiateur, et non le réconciliateur de porte-documents, est responsable de l’interrogation de l’utilisateur et de l’exécution des instructions de l’utilisateur.

Dans d’autres cas, l’intervention de l’utilisateur peut s’avérer nécessaire, par exemple, lorsque deux versions ont été modifiées de manière incompatible. Dans ce cas, l’initiateur ou le réconciliateur de porte-documents doit interroger l’utilisateur pour obtenir des instructions sur la façon de résoudre le conflit. En général, aucun initiateur ne peut s’appuyer sur l’exécution d’un rapprochement sans attendre une interaction de l’utilisateur. En revanche, les réconcilieurs ont la possibilité d’interagir avec l’utilisateur pour résoudre les conflits ou demander à l’initiateur de le faire.

### <a name="reconciling-embedded-objects"></a>Rapprochement des objets incorporés

Lors du rapprochement d’un document, le réconciliateur de porte-documents peut devenir un initiateur s’il découvre un objet incorporé d’un type qu’il ne peut pas rapprocher. Dans ce cas, le réconciliateur doit réconcilier de manière récursive chacun des objets incorporés et assumer toutes les responsabilités d’un initiateur.

Pour effectuer la récursivité, le réconciliateur de porte-documents charge l’objet et les requêtes pour l’interface appropriée. Le gestionnaire de l’objet doit prendre en charge l’interface. Si une méthode de l’interface retourne la \_ valeur OLE E \_ NOTRUNNING, le réconciliateur doit exécuter l’objet afin d’effectuer l’opération. Étant donné que le code des objets incorporés n’est pas toujours disponible, un réconciliateur doit fournir une solution pour cette condition. Par exemple, le réconciliateur peut inclure à la fois les anciennes et les nouvelles versions de l’objet incorporé dans la version conciliée. Le réconciliateur ne doit pas tenter d’effectuer un rapprochement entre les liens.

L’initiateur stocke les versions de documents en cours de fusion. Dans de nombreux cas, l’initiateur a accès au stockage de chaque version et enregistre le résultat de la réconciliation à l’aide d’un stockage similaire. Toutefois, l’initiateur peut parfois avoir un objet en mémoire pour lequel aucune version persistante n’est disponible. Cette situation peut se produire lorsqu’un document contenant des objets incorporés ouverts doit être concilié avant d’être enregistré. Dans ce cas, l’initiateur enregistre le résultat du rapprochement dans la version trouvée dans la mémoire.

L’initiateur utilise l’interface [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) pour lier (charger) la version fusionnée. L’initiateur utilise la méthode [IPersistStorage :: Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) si une version initiale a déjà été créée et utilise la méthode [IPersistStorage :: InitNew](/windows/win32/api/objidl/nf-objidl-ipersiststorage-initnew) pour la version initiale. Lorsque la version fusionnée est chargée, l’initiateur utilise [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour récupérer l’adresse de l’interface [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) . Cette interface donne à l’initiateur l’accès au stockage des résidus existants et lui donne la possibilité de créer un stockage pour les nouveaux résidus. L’initiateur dirige ensuite l’interface pour effectuer la réconciliation. En fait, l’initiateur interroge l’interface [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) avant IPersistStorage. Si le réconciliateur prend en charge IPersistFile, l’initiateur manipule le réplica via IPersistFile plutôt que les méthodes IPersistStorage. Cela permet de réconcilier les fichiers qui ne sont pas stockés en tant que documents composés.

Une fois le rapprochement terminé, l’initiateur peut enregistrer la version fusionnée à l’aide de l’interface [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) ou [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Lors du rapprochement, le réconciliateur de porte-documents crée des résidus en fonction des besoins et écrit leurs bits persistants dans le stockage. Si la version fusionnée est un flux, l’interface [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) transmise à [IPersistStorage :: Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) contient un flux nommé « contents » dont l’état de stockage est défini sur STATEBITS \_ Flat. (Vous pouvez définir les bits d’État à l’aide de la méthode [IStorage :: stat](/windows/win32/api/objidl/nf-objidl-istorage-stat) .) Après la fusion, l’initiateur enregistre la version fusionnée en écrivant les données de manière appropriée. Il doit s’assurer que STATEBITS \_ Flat est défini comme approprié pour le stockage.

### <a name="residues"></a>Résidus

L’initiateur indique s’il souhaite obtenir des résidus en définissant le paramètre *pstgNewResidues* sur une adresse valide lors de l’appel de la méthode [**IReconcilableObject :: réconcili**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) . Si le réconciliateur ne prend pas en charge la création de résidus, il doit retourner immédiatement la \_ valeur Rec E \_ noresidus, sauf si le paramètre *dwFlags* spécifie la valeur **\_ NORESIDUESOK RECONCILEF** .

Le réconciliateur de porte-documents retourne les résidus à l’initiateur en créant de nouveaux éléments de stockage et en les copiant dans le tableau pointé par *pstgNewResidues*. Pour les résidus de stockage structuré, le réconciliateur copie une interface [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) et, pour les résidus de stockage plat, il copie une interface [IStream](/windows/win32/api/objidl/nn-objidl-istream) ou IStorage avec l' \_ indicateur plat STATEBITS défini. Le réconciliateur utilise IStorage pour créer le stockage nécessaire, en utilisant [IStorage :: CreateStream,](/windows/win32/api/objidl/nf-objidl-istorage-createstream) pour créer un stockage plat pour un résidu qui est un flux et [IStorage :: CreateStorage](/windows/win32/api/objidl/nf-objidl-istorage-createstorage) pour créer un stockage structuré.

L’initiateur prépare *pstgNewResidues* afin qu’il ne contienne aucun élément dans la partie non réservée de l’espace de noms [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) . Le réconciliateur de porte-documents place chaque résidu dans un élément dont le nom correspond à l’ordre de sa version initiale. Par exemple, le premier résidu est contenu dans « 1 », le deuxième dans « 2 », et ainsi de suite. Si l’objet concilié lui-même produit un résidu, il se trouve dans l’élément nommé « 0 ».

Le réconciliateur de porte-documents valide chacun des éléments nouvellement créés individuellement, en veillant à ce que l’initiateur ait accès aux informations. Toutefois, le réconciliateur ne valide pas *pstgNewResidues* . L’initiateur est chargé de la valider ou de le supprimer.

## <a name="briefcase-reconciler-reference"></a>Référence du réconciliateur de porte-documents

Cette section contient des informations sur les interfaces de réconciliation. Lors de la gestion des erreurs, une méthode peut retourner uniquement les valeurs d’erreur qui sont explicitement définies comme valeurs de retour possibles. En outre, la méthode doit définir toutes les variables dont les adresses sont passées en tant que paramètres à la **valeur null** avant de retourner l’erreur.

### <a name="briefcase-reconciler-interfaces-and-methods"></a>Méthodes et interfaces du réconciliateur de porte-documents

-   [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) 
    -   -   [**IReconcilableObject::GetProgressFeedbackMaxEstimate**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-getprogressfeedbackmaxestimate)
        -   [**IReconcilableObject :: rapprocher**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile)

-   [**IReconcileInitiator**](ireconcileinitiator.md) 
    -   -   [**IReconcileInitiator::SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)
        -   [**IReconcileInitiator::SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback)

-   [**INotifyReplica**](/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica) 
    -   -   [**INotifyReplica::YouAreAReplica**](/windows/desktop/api/reconcil/nf-reconcil-inotifyreplica-youareareplica)

 

 