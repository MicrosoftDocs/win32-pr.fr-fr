---
description: Il existe plusieurs types de requêtes conçus pour interroger l’état des ressources.
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: Requêtes (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f450aa7015d4b66ad28b6c4d0632b2995bedd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845733"
---
# <a name="queries-direct3d-9"></a>Requêtes (Direct3D 9)

Il existe plusieurs types de requêtes conçus pour interroger l’état des ressources. L’état d’une ressource donnée comprend l’état de l’unité de traitement graphique (GPU), l’état du pilote ou l’état d’exécution. Pour comprendre la différence entre les différents types de requêtes, vous devez comprendre les États de requête. Le diagramme de transition d’état suivant explique chacun des États de requête.

![Diagramme montrant les transitions entre les États de requête](images/queries.png)

Le diagramme montre trois États, chacun défini par des cercles. Chaque ligne pleine est un événement piloté par l’application qui provoque une transition d’État. La ligne en pointillés est un événement piloté par les ressources qui bascule une requête de l’État émis à l’état signalé. Chacun de ces États a un objectif différent :

-   L’état signalé est comme un état inactif. L’objet de requête a été généré et attend que l’application émette la requête. Une fois qu’une requête est terminée et repassée à l’état signalé, la réponse à la requête peut être récupérée.
-   L’état de construction est comme une zone de transit pour une requête. À partir de l’État immeuble, une requête a été émise (en appelant [**D3DISSUE \_ Begin**](d3dissue-begin.md)) mais n’a pas encore été transportée à l’État émis. Lorsqu’une application émet une fin de requête (en appelant [**D3DISSUE \_ end**](d3dissue-end.md)), la requête passe à l’État émis.
-   L’État émis signifie que la ressource interrogée contrôle la requête. Une fois que la ressource a terminé son travail, la ressource fait passer l’ordinateur d’État à l’état signalé. Au cours de l’État émis, l’application doit interroger pour détecter la transition vers l’état signalé. Une fois la transition vers l’état signalé effectuée, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) retourne le résultat de la requête (par le biais d’un argument) à l’application.

Le tableau suivant répertorie les types de requêtes disponibles.



| Type de requête        | Événement de problème                                                                      | Mémoire tampon GetData                                                              | Runtime      | Début de requête implicite                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| BANDWIDTHTIMINGS  | [**D3DISSUE \_ Début**](d3dissue-begin.md), [ **D3DISSUE \_ fin**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS**](d3ddevinfo-d3d9bandwidthtimings.md) | Vente au détail/débogage | N/A                                              |
| CACHEUTILIZATION  | [**D3DISSUE \_ Début**](d3dissue-begin.md), [ **D3DISSUE \_ fin**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9CACHEUTILIZATION**](d3ddevinfo-d3d9cacheutilization.md) | Vente au détail/débogage | N/A                                              |
| ÉVÉNEMENT             | [**Fin de D3DISSUE \_**](d3dissue-end.md)                                            | BOOL                                                                        | Vente au détail/débogage | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| INTERFACETIMINGS  | [**D3DISSUE \_ Début**](d3dissue-begin.md), [ **D3DISSUE \_ fin**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9INTERFACETIMINGS**](d3ddevinfo-d3d9interfacetimings.md) | Vente au détail/débogage | N/A                                              |
| OCCLUSION         | [**D3DISSUE \_ Début**](d3dissue-begin.md), [ **D3DISSUE \_ fin**](d3dissue-end.md) | DWORD                                                                       | Vente au détail/débogage | N/A                                              |
| PIPELINETIMINGS   | [**D3DISSUE \_ Début**](d3dissue-begin.md), [ **D3DISSUE \_ fin**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9PIPELINETIMINGS**](d3ddevinfo-d3d9pipelinetimings.md)   | Vente au détail/débogage | N/A                                              |
| RESOURCEMANAGER   | [**Fin de D3DISSUE \_**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ ResourceManager**](d3ddevinfo-resourcemanager.md)           | Déboguer uniquement   | [**Présent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| timestamp         | [**Fin de D3DISSUE \_**](d3dissue-end.md)                                            | UINT64                                                                      | Vente au détail/débogage | N/A                                              |
| TIMESTAMPDISJOINT | [**D3DISSUE \_ Début**](d3dissue-begin.md), [ **D3DISSUE \_ fin**](d3dissue-end.md) | BOOL                                                                        | Vente au détail/débogage | N/A                                              |
| TIMESTAMPFREQ     | [**Fin de D3DISSUE \_**](d3dissue-end.md)                                            | UINT64                                                                      | Vente au détail/débogage | N/A                                              |
| VCACHE            | [**Fin de D3DISSUE \_**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ Vcache**](d3ddevinfo-vcache.md)                             | Vente au détail/débogage | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| VERTEXSTATS       | [**Fin de D3DISSUE \_**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ D3DVERTEXSTATS**](d3ddevinfo-d3dvertexstats.md)             | Déboguer uniquement   | [**Présent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| VERTEXTIMINGS     | [**D3DISSUE \_ Début**](d3dissue-begin.md), [ **D3DISSUE \_ fin**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9STAGETIMINGS**](d3ddevinfo-d3d9stagetimings.md)         | Vente au détail/débogage | N/A                                              |



 

Certaines des requêtes requièrent un événement de début et de fin, tandis que d’autres requièrent uniquement un événement de fin. Les requêtes qui requièrent uniquement un événement de fin commencent lorsqu’un autre événement implicite se produit (qui est listé dans le tableau). Toutes les requêtes retournent une réponse, à l’exception de la requête d’événement dont la réponse est toujours **true**. Une application utilise l’état de la requête ou le code de retour de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).

## <a name="create-a-query"></a>Créer une requête

Avant de créer une requête, vous pouvez vérifier si le runtime prend en charge les requêtes en appelant [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) avec un pointeur **null** comme suit :


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



Cette méthode retourne un code de réussite si une requête peut être créée ; Sinon, elle retourne un code d’erreur. Une fois l’opération [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) effectuée, vous pouvez créer un objet de requête comme suit :


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



Si cet appel a échoué, un objet de requête est créé. La requête est essentiellement inactive dans l’état signalé (avec une réponse non initialisée) en attente d’émission. Lorsque vous avez terminé avec la requête, libérez-la comme n’importe quelle autre interface.

## <a name="issue-a-query"></a>Émettre une requête

Une application modifie un état de requête en émettant une requête. Voici un exemple d’émission d’une requête :


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



Une requête dans l’état signalé suit une transition similaire à celle-ci lorsqu’elle est émise :



| Type de problème                                | Les transitions de requête vers le. . . |
|-------------------------------------------|--------------------------------|
| [**Début de D3DISSUE \_**](d3dissue-begin.md) | État de création.                |
| [**Fin de D3DISSUE \_**](d3dissue-end.md)     | État émis.                  |



 

Une requête dans l’état de génération suit une transition similaire à celle-ci lorsqu’elle est émise :



| Type de problème                                | Les transitions de requête vers le. . .                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [**Début de D3DISSUE \_**](d3dissue-begin.md) | (Aucune transition, reste dans l’état de construction. Redémarre le crochet de requête.) |
| [**Fin de D3DISSUE \_**](d3dissue-end.md)     | État émis.                                                             |



 

Une requête dans l’État émis passera comme suit lorsqu’elle est émise :



| Type de problème                                | Les transitions de requête vers le. . .                    |
|-------------------------------------------|---------------------------------------------------|
| [**Début de D3DISSUE \_**](d3dissue-begin.md) | Génération de l’État et redémarrage du crochet de requête.    |
| [**Fin de D3DISSUE \_**](d3dissue-end.md)     | État émis après l’abandon de la requête existante. |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a>Vérifier l’état de la requête et obtenir la réponse à la requête

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) effectue deux opérations :

1.  Retourne l’état de requête dans le code de retour.
2.  Retourne la réponse à la requête dans *pData*.

À partir de chacun des trois États de requête, Voici les codes de retour [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) :



| État de requête | GetData (code de retour) |
|-------------|---------------------|
| Signalé    | \_OK               |
| Génération    | Code d'erreur          |
| Émis      | S \_ false            |



 

Par exemple, lorsqu’une requête est dans l’État émis et que la réponse à la requête n’est pas disponible, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) retourne S \_ false. Lorsque la ressource termine son travail et que l’application a émis une fin de requête, la ressource fait passer la requête à l’état signalé. À partir de l’état signalé, **GetData** retourne \_ « S OK », ce qui signifie que la réponse à la requête est également retournée dans *pData*. Par exemple, voici la séquence d’événements pour retourner le nombre de pixels dessinés dans une séquence de rendu :

-   Création de la requête
-   Émettez un événement de début.
-   Dessinez un texte.
-   Émettez un événement de fin.

Voici la séquence de code correspondante :


```
IDirect3DQuery9* pOcclusionQuery;
DWORD numberOfPixelsDrawn;

m_pD3DDevice->CreateQuery(D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery);

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_BEGIN);

// API render loop
...
Draw(...)
...

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pOcclusionQuery->GetData( &numberOfPixelsDrawn, 
                                  sizeof(DWORD), D3DGETDATA_FLUSH ))
    ;
```



Ces lignes de code effectuent plusieurs opérations :

-   Appelez [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) pour retourner le nombre de pixels dessinés.
-   Spécifiez [**D3DGETDATA \_ flush**](d3dgetdata-flush.md) pour permettre à la ressource de faire passer la requête à l’état signalé.
-   Interrogez la ressource de requête en appelant [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) à partir d’une boucle. Tant que **GetData** retourne S \_ false, cela signifie que la ressource n’a pas encore retourné la réponse.

La valeur de retour de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) vous indique essentiellement l’état de la requête. Les valeurs possibles sont S \_ OK, s \_ false et une erreur. N’appelez pas **GetData** sur une requête qui se trouve dans l’État Building.

-   S \_ OK signifie que la ressource (GPU ou pilote, ou Runtime) est terminée. La requête revient à l’état signalé. La réponse (le cas échéant) est retournée par [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).
-   S \_ false signifie que la ressource (GPU ou pilote, ou Runtime) ne peut pas encore retourner une réponse. Cela peut être dû au fait que le GPU n’est pas terminé ou n’a pas encore vu le travail.
-   Une erreur signifie que la requête a généré une erreur à partir de laquelle elle ne peut pas être récupérée. Cela peut être le cas si l’appareil est perdu au cours d’une requête. Une fois qu’une requête a généré une erreur (autre que la \_ valeur S false), la requête doit être recréée, ce qui permet de redémarrer la séquence de requête à partir de l’état signalé.

Au lieu de spécifier [**D3DGETDATA \_ flush**](d3dgetdata-flush.md), qui fournit des informations plus récentes, vous pouvez fournir zéro qui est un contrôle plus clair si la requête est dans l’État émis. Si vous fournissez zéro, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) n’efface pas le tampon de commande. Pour cette raison, il faut veiller à éviter les boucles infinate (pour plus d’informations, consultez **GetData** ). Dans la mesure où le Runtime met en file d’attente le travail dans le tampon de commande, le **\_ vidage D3DGETDATA** est un mécanisme permettant de vider le tampon de commande sur le pilote (et par conséquent, le GPU ; consultez [profilage des appels d’API Direct3D avec précision](accurately-profiling-direct3d-api-calls.md)). Pendant le vidage de la mémoire tampon de commande, une requête peut passer à l’état signalé.

## <a name="example-an-event-query"></a>Exemple : une requête d’événement

Une requête d’événement ne prend pas en charge un événement de début.

-   Création de la requête
-   Émettez un événement de fin.
-   Interroger jusqu’à ce que le GPU soit inactif.
-   Émettez un événement de fin.


```
IDirect3DQuery9* pEventQuery = NULL;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

... // API calls

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
```



Il s’agit de la séquence de commandes utilisée par une requête d’événement pour profiler les appels de l’interface de programmation d’applications (API) (consultez Profiler [avec précision les appels d’API Direct3D (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)). Cette séquence utilise des marqueurs pour aider à contrôler la quantité de travail dans le tampon de commande.

Notez que les applications doivent prêter une attention particulière au grand coût associé au vidage du tampon de commande, car cela amène le système d’exploitation à basculer en mode noyau, ce qui se traduit par une baisse notable des performances. Les applications doivent également être conscientes du gaspillage des cycles processeur en attendant la fin des requêtes.

Les requêtes sont une optimisation à utiliser pendant le rendu pour améliorer les performances. Par conséquent, il n’est pas judicieux de consacrer du temps à attendre la fin d’une requête. Si une requête est émise et si les résultats ne sont pas encore prêts au moment où l’application les vérifie, la tentative d’optimisation n’a pas été effectuée et le rendu doit se poursuivre normalement.

L’exemple classique est l’élimination de l’occlusion. Au lieu de la boucle **while** ci-dessus, une application utilisant des requêtes peut implémenter l’élimination d’occlusion pour vérifier si une requête s’est terminée au moment où elle a besoin du résultat. Si la requête n’est pas terminée, poursuivez (dans le pire des cas) comme si l’objet testé par rapport à n’est pas bloqués (c.-à-d. qu’elle est visible) et qu’elle est rendue. Le code doit ressembler à ce qui suit.


```
IDirect3DQuery9* pOcclusionQuery = NULL;
m_pD3DDevice->CreateQuery( D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery );

// Add a begin marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_BEGIN );

... // API calls

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_END );

// Avoid flushing and letting the CPU go idle by not using a while loop.
// Check if queries are finished:
DWORD dwOccluded = 0;
if( S_FALSE == pOcclusionQuery->GetData( &dwOccluded, sizeof(DWORD), 0 ) )
{
    // Query is not done yet or object not occluded; avoid flushing/wait by continuing with worst-case scenario
    pSomeComplexMesh->Render();
}
else if( dwOccluded != 0 )
{
    // Query is done and object is not occluded.
    pSomeComplexMesh->Render();
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées](advanced-topics.md)
</dt> </dl>

 

 
