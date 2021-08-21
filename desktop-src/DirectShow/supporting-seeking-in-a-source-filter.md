---
description: cette rubrique décrit comment implémenter la recherche dans un filtre de source Microsoft DirectShow. Elle utilise l’exemple de filtre ball comme point de départ et décrit le code supplémentaire nécessaire pour prendre en charge la recherche dans ce filtre.
ms.assetid: a2b4be09-2fd6-4aac-8ad6-c3d62377c1f2
title: Prise en charge de la recherche dans un filtre source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d92c52ff4bde3ea75b156e5521af9825b0902df38f0d0c6bc23cc7be99c37a55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072353"
---
# <a name="supporting-seeking-in-a-source-filter"></a>Prise en charge de la recherche dans un filtre source

cette rubrique décrit comment implémenter la recherche dans un filtre de source Microsoft DirectShow. Elle utilise l’exemple de [filtre ball](ball-filter-sample.md) comme point de départ et décrit le code supplémentaire nécessaire pour prendre en charge la recherche dans ce filtre.

L’exemple de [filtre ball](ball-filter-sample.md) est un filtre source qui crée une balle de rebond animée. Cet article explique comment ajouter des fonctionnalités de recherche à ce filtre. Une fois que vous avez ajouté cette fonctionnalité, vous pouvez afficher le filtre dans GraphEdit et contrôler la balle en faisant glisser le curseur GraphEdit.

Cette rubrique contient les sections suivantes :

-   [Vue d’ensemble de la recherche dans DirectShow](#overview-of-seeking-in-directshow)
-   [Aperçu rapide du filtre de la balle](#quick-overview-of-the-ball-filter)
-   [Modification du filtre de balle pour la recherche](#modifying-the-ball-filter-for-seeking)
-   [Limitations de la classe CSourceSeeking](#limitations-of-the-csourceseeking-class)

## <a name="overview-of-seeking-in-directshow"></a>Vue d’ensemble de la recherche dans DirectShow

une application recherche le graphique de filtre en appelant une méthode [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) sur le gestionnaire de Graph de filtre. le gestionnaire de Graph de filtre distribue ensuite l’appel à chaque convertisseur dans le graphique. Chaque convertisseur envoie l’appel en amont, par le biais de la broche de sortie du filtre amont suivant. L’appel se déplace en amont jusqu’à ce qu’il atteigne un filtre qui peut exécuter la commande Seek, en général un filtre source ou un filtre d’analyseur. En général, le filtre qui est à l’origine de l’horodatage gère également la recherche.

Un filtre répond à une commande Seek comme suit :

1.  Le filtre vide le graphique. Cela efface toutes les données obsolètes du graphique, ce qui améliore la réactivité. Sinon, les exemples qui ont été mis en mémoire tampon avant la commande Seek peuvent être remis.
2.  Le filtre appelle [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) pour informer les filtres en aval de la nouvelle heure d’arrêt, de l’heure de début et de la vitesse de lecture.
3.  Le filtre définit ensuite l’indicateur de discontinuité sur le premier échantillon après la commande Seek.

Les horodatages commencent à zéro après toute commande Seek (y compris les changements de taux).

## <a name="quick-overview-of-the-ball-filter"></a>Aperçu rapide du filtre de la balle

Le filtre bille est une source push, ce qui signifie qu’il utilise un thread de travail pour remettre des exemples en aval, par opposition à une source pull, qui attend passivement un filtre en aval pour demander des exemples. Le filtre balle est construit à partir de la classe [**CSource**](csource.md) , et sa broche de sortie est créée à partir de la classe [**CSourceStream**](csourcestream.md) . La classe **CSourceStream** crée le thread de travail qui pilote le workflow de données. Ce thread entre dans une boucle qui obtient des échantillons de l’allocateur, les remplit avec les données et les remet en aval.

La majeure partie de l’action dans [**CSourceStream**](csourcestream.md) se produit dans la méthode [**CSourceStream :: FillBuffer**](csourcestream-fillbuffer.md) , que la classe dérivée implémente. L’argument de cette méthode est un pointeur vers l’exemple à remettre. L’implémentation du filtre ball de **FillBuffer** récupère l’adresse de l’exemple de mémoire tampon et l’insère directement dans la mémoire tampon en définissant des valeurs de pixel individuelles. (Le dessin est effectué par une classe d’assistance, CBall, ce qui vous permet d’ignorer les détails concernant les profondeurs de bits, les palettes, etc.).

## <a name="modifying-the-ball-filter-for-seeking"></a>Modification du filtre de balle pour la recherche

Pour rendre le filtre de balle accessible, utilisez la classe [**CSourceSeeking**](csourceseeking.md) , qui est conçue pour l’implémentation de la recherche dans les filtres avec une seule broche de sortie. Ajoutez la classe **CSourceSeeking** à la liste d’héritage pour la classe CBallStream :


```C++
class CBallStream :  // Defines the output pin.
    public CSourceStream, public CSourceSeeking
```



En outre, vous devrez ajouter un initialiseur pour [**CSourceSeeking**](csourceseeking.md) au constructeur CBallStream :


```C++
    CSourceSeeking(NAME("SeekBall"), (IPin*)this, phr, &m_cSharedState),
```



Cette instruction appelle le constructeur de base pour [**CSourceSeeking**](csourceseeking.md). Les paramètres sont un nom, un pointeur vers le code confidentiel propriétaire, une valeur **HRESULT** et l’adresse d’un objet de section critique. Le nom est utilisé uniquement pour le débogage, et la macro de [**nom**](name.md) se compile en une chaîne vide dans les builds de vente au détail. Le code PIN hérite directement de **CSourceSeeking**. le deuxième paramètre est donc un pointeur vers lui-même, casté en pointeur [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) . La valeur **HRESULT** est ignorée dans la version actuelle des classes de base ; Il reste pour la compatibilité avec les versions précédentes. La section critique protège les données partagées, telles que l’heure de début, l’heure d’arrêt et la vitesse de lecture actuelles.

Ajoutez l’instruction suivante à l’intérieur du constructeur [**CSourceSeeking**](csourceseeking.md) :


```C++
m_rtStop = 60 * UNITS;
```



La variable *m \_ rtStop* spécifie l’heure d’arrêt. Par défaut, la valeur est \_ I64 \_ Max/2, soit environ 14 600 ans. L’instruction précédente la définit sur une durée plus restrictive de 60 secondes.

Deux variables membres supplémentaires doivent être ajoutées à CBallStream :


```C++
BOOL            m_bDiscontinuity; // If true, set the discontinuity flag.
REFERENCE_TIME  m_rtBallPosition; // Position of the ball. 
```



Après chaque commande Seek, le filtre doit définir l’indicateur discontinu sur l’exemple suivant en appelant [**IMediaSample :: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity). La variable *m \_ bDiscontinuity* effectue le suivi de ce. La variable *m \_ rtBallPosition* spécifie la position de la balle dans le cadre de la vidéo. Le filtre boule d’origine calcule la position à partir du temps de flux, mais le temps de flux est redéfini à zéro après chaque commande Seek. Dans un flux de recherche, la position absolue est indépendante du temps de flux.

### <a name="queryinterface"></a>QueryInterface

La classe [**CSourceSeeking**](csourceseeking.md) implémente l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . Pour exposer cette interface aux clients, remplacez la méthode [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) :


```C++
STDMETHODIMP CBallStream::NonDelegatingQueryInterface
    (REFIID riid, void **ppv)
{
    if( riid == IID_IMediaSeeking ) 
    {
        return CSourceSeeking::NonDelegatingQueryInterface( riid, ppv );
    }
    return CSourceStream::NonDelegatingQueryInterface(riid, ppv);
}
```



la méthode est appelée « NonDelegating » en raison de la façon dont les classes de base DirectShow prennent en charge l’agrégation COM (component Object Model). pour plus d’informations, consultez la rubrique « comment implémenter IUnknown » dans le kit de développement logiciel (SDK) DirectShow.

### <a name="seeking-methods"></a>Méthodes de recherche

La classe [**CSourceSeeking**](csourceseeking.md) gère plusieurs variables membres relatives à la recherche.



| Variable          | Description   | Valeur par défaut  |
|-------------------|---------------|----------------|
| *m \_ rtStart*      | Heure de début    | Zéro           |
| *m \_ rtStop*       | Heure d’arrêt     | \_I64 \_ Max/2 |
| *m \_ dRateSeeking* | Vitesse de lecture | 1.0            |



 

L’implémentation [**CSourceSeeking**](csourceseeking.md) de [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) met à jour les heures de démarrage et d’arrêt, puis appelle deux méthodes virtuelles pures sur la classe dérivée, [**CSourceSeeking :: modifiez l'**](csourceseeking-changestart.md) et [**CSourceSeeking :: ChangeStop**](csourceseeking-changestop.md). L’implémentation de [**IMediaSeeking ::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) est similaire : elle met à jour la vitesse de lecture, puis appelle la méthode virtuelle pure [**CSourceSeeking :: ChangeRate**](csourceseeking-changerate.md). Dans chacune de ces méthodes virtuelles, le code confidentiel doit effectuer les opérations suivantes :

1.  Appelez [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) pour démarrer le vidage des données.
2.  Arrêtez le thread de streaming.
3.  Appelez [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).
4.  Redémarrez le thread de streaming.
5.  Appelez [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).
6.  Définissez l’indicateur de discontinuité sur l’exemple suivant.

L’ordre de ces étapes est essentiel, car le thread de streaming peut se bloquer pendant qu’il attend de remettre un exemple ou d’obtenir un nouvel exemple. La méthode [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) garantit que le thread de diffusion en continu n’est pas bloqué et, par conséquent, ne se bloque pas à l’étape 2. L’appel [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) informe les filtres en aval qu’ils attendent de nouveaux exemples, donc ils ne les rejettent pas lorsque le thread redémarre à l’étape 4.

La méthode privée suivante effectue les étapes 1 à 4 :


```C++
void CBallStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        // Shut down the thread and stop pushing data.
        Stop();
        DeliverEndFlush();
        // Restart the thread and start pushing data again.
        Pause();
    }
}
```



Lorsque le thread de streaming redémarre, il appelle la méthode [**CSourceStream :: OnThreadStartPlay**](csourcestream-onthreadstartplay.md) . Remplacez cette méthode pour effectuer les étapes 5 et 6 :


```C++
HRESULT CBallStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



Dans la méthode [**Modifiez l'**](csourceseeking-changestart.md) , définissez le temps de flux sur zéro et la position de la balle sur la nouvelle heure de début. Appelez ensuite CBallStream :: UpdateFromSeek :


```C++
HRESULT CBallStream::ChangeStart( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_rtSampleTime = 0;
        m_rtBallPosition = m_rtStart;
    }
    UpdateFromSeek();
    return S_OK;
}
```



Dans la méthode [**ChangeStop**](csourceseeking-changestop.md) , appelez CBallStream :: UpdateFromSeek si la nouvelle heure d’arrêt est inférieure à la position actuelle. Dans le cas contraire, l’heure d’arrêt est toujours à l’avenir, il n’est donc pas nécessaire de vider le graphique.


```C++
HRESULT CBallStream::ChangeStop( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        if (m_rtBallPosition < m_rtStop)
        {
            return S_OK;
        }
    }

    // We're already past the new stop time. Flush the graph.
    UpdateFromSeek();
    return S_OK;
}
```



Pour les changements de taux, la méthode [**CSourceSeeking ::**](csourceseeking-setrate.md) se, définit *m \_ dRateSeeking* sur le nouveau taux (en ignorant l’ancienne valeur) avant d’appeler [**ChangeRate**](csourceseeking-changerate.md). Malheureusement, si l’appelant a donné un taux non valide (par exemple, inférieur à zéro), il est trop tard au moment de l’appel de **ChangeRate** . Une solution consiste à remplacer seet à **vérifier les taux** valides :


```C++
HRESULT CBallStream::SetRate(double dRate)
{
    if (dRate <= 1.0)
    {
        return E_INVALIDARG;
    }
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_dRateSeeking = dRate;
    }
    UpdateFromSeek();
    return S_OK;
}
// Now ChangeRate won't ever be called, but it's pure virtual, so it needs
// a dummy implementation.
HRESULT CBallStream::ChangeRate() { return S_OK; }
```



### <a name="drawing-in-the-buffer"></a>Dessin dans la mémoire tampon

Voici la version modifiée de [**CSourceStream :: FillBuffer**](csourcestream-fillbuffer.md), la routine qui dessine la balle sur chaque image :


```C++
HRESULT CBallStream::FillBuffer(IMediaSample *pMediaSample)
{
    BYTE *pData;
    long lDataLen;
    pMediaSample->GetPointer(&pData);
    lDataLen = pMediaSample->GetSize();
    {
        CAutoLock cAutoLockShared(&m_cSharedState);
        if (m_rtBallPosition >= m_rtStop) 
        {
            // End of the stream.
            return S_FALSE;
        }
        // Draw the ball in its current position.
        ZeroMemory( pData, lDataLen );
        m_Ball->MoveBall(m_rtBallPosition);
        m_Ball->PlotBall(pData, m_BallPixel, m_iPixelSize);
        
        // The sample times are modified by the current rate.
        REFERENCE_TIME rtStart, rtStop;
        rtStart = static_cast<REFERENCE_TIME>(
                      m_rtSampleTime / m_dRateSeeking);
        rtStop  = rtStart + static_cast<int>(
                      m_iRepeatTime / m_dRateSeeking);
        pMediaSample->SetTime(&rtStart, &rtStop);

        // Increment for the next loop.
        m_rtSampleTime += m_iRepeatTime;
        m_rtBallPosition += m_iRepeatTime;
    }
    pMediaSample->SetSyncPoint(TRUE);
    if (m_bDiscontinuity) 
    {
        pMediaSample->SetDiscontinuity(TRUE);
        m_bDiscontinuity = FALSE;
    }
    return NOERROR;
}
```



Les principales différences entre cette version et l’original sont les suivantes :

-   Comme indiqué précédemment, la variable *m \_ rtBallPosition* est utilisée pour définir la position de la balle, plutôt que le temps de flux.
-   Après avoir appuyé sur la section critique, la méthode vérifie si la position actuelle dépasse l’heure d’arrêt. Si c’est le cas, elle retourne **S \_ false**, ce qui indique à la classe de base d’arrêter l’envoi de données et de fournir une notification de fin de flux.
-   Les horodatages sont divisés par le taux actuel.
-   Si *m \_ bDiscontinuity* a la **valeur true**, la méthode définit l’indicateur de discontinuité sur l’exemple.

Il existe une autre différence mineure. Étant donné que la version d’origine s’appuie sur un seul tampon, elle remplit la totalité de la mémoire tampon avec des zéros une fois, au début de la diffusion en continu. Après cela, il efface simplement la balle de sa position précédente. Toutefois, cette optimisation révèle un léger bogue dans le filtre balle. Lorsque la méthode [**CBaseOutputPin ::D ecideallocator**](cbaseoutputpin-decideallocator.md) appelle [**IMemInputPin :: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), elle affecte à l’indicateur de lecture seule la **valeur false**. Par conséquent, le filtre en aval est libre d’écrire sur la mémoire tampon. Une solution consiste à remplacer **DecideAllocator** afin qu’il affecte à l’indicateur de lecture seule la **valeur true**. Toutefois, pour des raisons de simplicité, la nouvelle version supprime tout simplement l’optimisation. Au lieu de cela, cette version remplit la mémoire tampon avec des zéros à chaque fois.

### <a name="miscellaneous-changes"></a>Modifications diverses

Dans la nouvelle version, ces deux lignes sont supprimées du constructeur CBall :


```C++
    m_iRandX = rand();
    m_iRandY = rand();
```



Le filtre boule d’origine utilise ces valeurs pour ajouter du caractère aléatoire à la position initiale de la balle. Dans le cadre de nos objectifs, nous voulons que la balle soit déterministe. En outre, certaines variables ont été modifiées des objets [**CRefTime**](creftime.md) en variables de [**\_ temps de référence**](reference-time.md) . (La classe **CRefTime** est un wrapper léger pour une valeur de **\_ temps de référence** .) Enfin, l’implémentation de [**IQualityControl :: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) a été légèrement modifiée. vous pouvez consulter le code source pour plus d’informations.

## <a name="limitations-of-the-csourceseeking-class"></a>Limitations de la classe CSourceSeeking

La classe [**CSourceSeeking**](csourceseeking.md) n’est pas destinée aux filtres avec plusieurs broches de sortie, en raison de problèmes de communication entre les broches. Par exemple, imaginez un filtre d’analyseur qui reçoit un flux audio/vidéo entrelacé, divise le flux en ses composants audio et vidéo et diffuse la vidéo d’une broche de sortie et de l’audio d’une autre. Les deux broches de sortie reçoivent chaque commande Seek, mais le filtre ne doit effectuer une recherche qu’une seule fois par commande Seek. La solution consiste à désigner l’un des codes confidentiels pour contrôler la recherche et à ignorer les commandes de recherche reçues par l’autre code PIN.

Toutefois, après la commande Seek, les deux codes confidentiels doivent vider les données. Pour compliquer davantage les choses, la commande Seek se produit sur le thread d’application, et non sur le thread de streaming. Par conséquent, vous devez vous assurer qu’aucun code confidentiel n’est bloqué et qu’il attend qu’un appel [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) soit retourné, ou qu’il peut provoquer un interblocage. Pour plus d’informations sur le vidage thread-safe dans les codes confidentiels, consultez [threads et sections critiques](threads-and-critical-sections.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture de filtres source](writing-source-filters.md)
</dt> </dl>

 

 



