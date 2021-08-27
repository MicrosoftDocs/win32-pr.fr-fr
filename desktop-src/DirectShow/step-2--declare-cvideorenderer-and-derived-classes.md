---
description: Cette rubrique est l’étape 2 de la lecture audio/vidéo du didacticiel dans DirectShow.
ms.assetid: 61106781-d10c-41a8-993e-121e0a1e4c4d
title: 'Étape 2 : déclarer CVideoRenderer et les classes dérivées'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fae4c9c391a13acd0ede06b9a74c3b09bd264a6b74c42d7f6c7ca5e9dbb17051
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050359"
---
# <a name="step-2-declare-cvideorenderer-and-derived-classes"></a>Étape 2 : déclarer CVideoRenderer et les classes dérivées

Cette rubrique est l’étape 2 de la [lecture audio/vidéo du didacticiel dans DirectShow](audio-video-playback-in-directshow.md). le code complet est présenté dans la rubrique [exemple de lecture DirectShow](directshow-playback-example.md).

DirectShow fournit plusieurs filtres différents qui restituent la vidéo :

-   [**Filtre de convertisseur vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR)
-   [Filtre de convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) (VMR-9)
-   [Filtre de convertisseur de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7)

Pour plus d’informations sur les différences entre ces filtres, consultez [choix du convertisseur vidéo approprié](choosing-the-right-renderer.md).

Dans ce didacticiel, la classe abstraite suivante est utilisée pour encapsuler le filtre de convertisseur vidéo.


```C++
// Abstract class to manage the video renderer filter.
// Specific implementations handle the VMR-7, VMR-9, or EVR filter.

class CVideoRenderer
{
public:
    virtual ~CVideoRenderer() {};
    virtual BOOL    HasVideo() const = 0;
    virtual HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd) = 0;
    virtual HRESULT FinalizeGraph(IGraphBuilder *pGraph) = 0;
    virtual HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc) = 0;
    virtual HRESULT Repaint(HWND hwnd, HDC hdc) = 0;
    virtual HRESULT DisplayModeChanged() = 0;
};
```



Remarques :

-   La `HasVideo` méthode retourne la **valeur true** si le convertisseur vidéo a été créé.
-   La `AddToGraph` méthode ajoute le convertisseur vidéo au graphique de filtre.
-   La `FinalizeGraph` méthode termine l’étape de création de graphiques.
-   La `UpdateVideoWindow` méthode met à jour le rectangle de destination de la vidéo.
-   La `Repaint` méthode redessine le frame vidéo actuel.
-   La `DisplayModeChanged` méthode gère les modifications du mode d’affichage.

Chacune de ces méthodes est décrite en détail plus loin dans ce didacticiel.

Ensuite, déclarez une classe dérivée pour encapsuler chacun des trois convertisseurs vidéo : EVR, VMR-9 et VMR-7.

### <a name="cevr-class"></a>CEVR, classe

La `CEVR` classe gère le EVR. Elle contient un pointeur vers les interfaces [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) et [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) de EVR.


```C++
// Manages the EVR video renderer filter.

class CEVR : public CVideoRenderer
{
    IBaseFilter            *m_pEVR;
    IMFVideoDisplayControl *m_pVideoDisplay;

public:
    CEVR();
    ~CEVR();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr9-class"></a>CVMR9, classe

La `CVMR9` classe gère VMR-9. Il contient un pointeur vers l’interface [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .


```C++
// Manages the VMR-9 video renderer filter.

class CVMR9 : public CVideoRenderer
{
    IVMRWindowlessControl9 *m_pWindowless;

public:
    CVMR9();
    ~CVMR9();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr7-class"></a>CVMR7, classe

La `CVMR7` classe gère VMR-7. Il contient un pointeur vers l’interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .


```C++
// Manages the VMR-7 video renderer filter.

class CVMR7 : public CVideoRenderer
{
    IVMRWindowlessControl   *m_pWindowless;

public:
    CVMR7();
    ~CVMR7();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



[Étape 3 : générer le filtre Graph](step-3--build-the-filter-graph.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo en DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Utilisation du convertisseur de mixage vidéo](using-the-video-mixing-renderer.md)
</dt> <dt>

[Rendu vidéo](video-rendering.md)
</dt> </dl>

 

 
