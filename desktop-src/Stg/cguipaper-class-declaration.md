---
title: Déclaration de la classe CGuiPaper
description: Déclaration de la classe CGuiPaper
ms.assetid: b772d056-bf89-46a8-9462-21772cf96dfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d684618eea78247b94ed03223cfce45d2cc713f5507b1e290731d3451212b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663519"
---
# <a name="cguipaper-class-declaration"></a>Déclaration de la classe CGuiPaper

Voici la déclaration de la classe **CGuiPaper** à partir de GUIPAPER. H.


```C++
class CGuiPaper
  {
    public:
      CGuiPaper(void);
      ~CGuiPaper(void);
      BOOL Init(HINSTANCE hInst, HWND hWnd, TCHAR* pszCmdLineFile);
      HRESULT DrawOn(void);
      HRESULT DrawOff(void);
      HRESULT ClearWin(void);
      HRESULT PaintWin(void);
      HRESULT Erase(void);
      HRESULT Resize(WORD wWidth, WORD wHeight);
      HRESULT InkWidth(SHORT nInkWidth);
      HRESULT InkColor(COLORREF crInkColor);
      HRESULT InkSaving(BOOL bInkSaving);
      HRESULT InkStart(SHORT nX, SHORT nY);
      HRESULT InkDraw(SHORT nX, SHORT nY);
      HRESULT InkStop(SHORT nX, SHORT nY);
      HRESULT ConnectPaperSink(void);
      HRESULT DisconnectPaperSink(void);
      HRESULT Load(void);
      HRESULT Save(void);
      int     AskSave(void);
      HRESULT Open(void);
      HRESULT SaveAs(void);
      COLORREF PickColor(void);

    private:
      HINSTANCE  m_hInst;
      HWND       m_hWnd;
      HDC        m_hDC;
      RECT       m_WinRect;
      IPaper*    m_pIPaper;
      SHORT      m_nLockKey;
      HPEN       m_hPen;
      SHORT      m_nInkWidth;
      COLORREF   m_crInkColor;
      BOOL       m_bInkSaving;
      BOOL       m_bInking;
      BOOL       m_bPainting;
      POINT      m_OldPos;
      IUnknown*  m_pCOPaperSink;
      DWORD      m_dwPaperSink;
      BOOL       m_bDirty;
      CPapFile*    m_pPapFile;
      OPENFILENAME m_ofnFile;
      TCHAR        m_szFileFilter[MAX_PATH];
      TCHAR        m_szFileName[MAX_PATH];
      TCHAR        m_szFileTitle[MAX_PATH];
      CHOOSECOLOR  m_ChooseColor;
      COLORREF     m_acrCustColors[16];

      IConnectionPoint* GetConnectionPoint(REFIID riid);
  };
```



**CGuiPaper** conserve les propriétés de l’interface graphique utilisateur actuelles pour le papier dessiné. Les membres **m \_ crInkColor**, **m \_ crInkWidth** et **m \_ WinRect** contiennent des valeurs pour la couleur d’encre actuelle, la largeur de l’encre et le rectangle de dessin. Le **membre \_ HWND de m** stocke le descripteur dans la fenêtre où la peinture est effectuée.

La peinture réelle des images s’effectue à l’aide d’un handle vers un contexte de périphérique situé dans le membre **m \_ HDC**. Un handle vers le stylet de dessin actuel est conservé dans le membre **m \_ hPen**. Le stylet est détruit et recréé lorsque sa couleur ou sa largeur est modifiée par l’utilisateur.

Les membres **m \_ pCOPaperSink** et **m \_ dwPaperSink** contiennent les valeurs nécessaires à la connexion au colivre pour recevoir des notifications entrantes via l’interface [**IPaperSink**](ipapersink-methods.md) . Le membre **m \_ bDirty** contient un indicateur qui indique que l’utilisateur a modifié le dessin et qu’il ne reflète plus les données stockées dans son fichier.

Le membre **m \_ pIPaper** contient le pointeur d’interface principal vers l’objet du codocument. Toutes les fonctionnalités du colivre sont accessibles via ce pointeur.

Le membre **m \_ nLockKey** est utilisé pour prendre en charge un modèle de verrouillage client qui est utilisé avec plusieurs clients pour permettre à un client d’accéder de façon exclusive à un objet de codocument partagé. Le codocument affecte **m \_ nLockKey** lors d’un appel [**IPaper**](ipaper-methods.md)::**Lock** et est transmis en tant que paramètre par le client lors d’appels ultérieurs au codocument. Le colivreur effectue le travail dans ces appels uniquement si la clé de verrouillage transmise correspond à la dernière remise de la clé à un client par le biais du colivre.

Le membre **m \_ pPapFile** contient un pointeur vers un objet [**CPapFile**](cpapfile-class-and-methods.md) . Il s’agit d’un objet C++ qui encapsule les opérations de chargement et d’enregistrement sur un fichier composé de stockage structuré. **CPapFile** fonctionne avec l’objet du coarticle basé sur le serveur sous-jacent pour charger et enregistrer les données de dessin du plan.

 

 




