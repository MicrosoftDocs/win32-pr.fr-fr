---
title: Déclaration de la classe CGuiPaper
description: Déclaration de la classe CGuiPaper
ms.assetid: b772d056-bf89-46a8-9462-21772cf96dfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269694b83804f3e85cd8654cd2a1be843396a2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028741"
---
# <a name="cguipaper-class-declaration"></a><span data-ttu-id="7618d-103">Déclaration de la classe CGuiPaper</span><span class="sxs-lookup"><span data-stu-id="7618d-103">CGuiPaper Class Declaration</span></span>

<span data-ttu-id="7618d-104">Voici la déclaration de la classe **CGuiPaper** à partir de GUIPAPER. H.</span><span class="sxs-lookup"><span data-stu-id="7618d-104">The following is the **CGuiPaper** class declaration from GUIPAPER.H.</span></span>


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



<span data-ttu-id="7618d-105">**CGuiPaper** conserve les propriétés de l’interface graphique utilisateur actuelles pour le papier dessiné.</span><span class="sxs-lookup"><span data-stu-id="7618d-105">**CGuiPaper** maintains the current GUI properties for the drawing paper.</span></span> <span data-ttu-id="7618d-106">Les membres **m \_ crInkColor**, **m \_ crInkWidth** et **m \_ WinRect** contiennent des valeurs pour la couleur d’encre actuelle, la largeur de l’encre et le rectangle de dessin.</span><span class="sxs-lookup"><span data-stu-id="7618d-106">Members **m\_crInkColor**, **m\_crInkWidth**, and **m\_WinRect** contain values for the current ink color, ink width, and drawing rectangle.</span></span> <span data-ttu-id="7618d-107">Le **membre \_ HWND de m** stocke le descripteur dans la fenêtre où la peinture est effectuée.</span><span class="sxs-lookup"><span data-stu-id="7618d-107">The **m\_hWnd** member stores the handle to the window where painting is done.</span></span>

<span data-ttu-id="7618d-108">La peinture réelle des images s’effectue à l’aide d’un handle vers un contexte de périphérique situé dans le membre **m \_ HDC**.</span><span class="sxs-lookup"><span data-stu-id="7618d-108">The actual painting of images is done using a handle to a device context held in member **m\_hDC**.</span></span> <span data-ttu-id="7618d-109">Un handle vers le stylet de dessin actuel est conservé dans le membre **m \_ hPen**.</span><span class="sxs-lookup"><span data-stu-id="7618d-109">A handle to the current drawing pen is kept in member **m\_hPen**.</span></span> <span data-ttu-id="7618d-110">Le stylet est détruit et recréé lorsque sa couleur ou sa largeur est modifiée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7618d-110">The pen is destroyed and recreated when its color or width is changed by the user.</span></span>

<span data-ttu-id="7618d-111">Les membres **m \_ pCOPaperSink** et **m \_ dwPaperSink** contiennent les valeurs nécessaires à la connexion au colivre pour recevoir des notifications entrantes via l’interface [**IPaperSink**](ipapersink-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="7618d-111">Members **m\_pCOPaperSink** and **m\_dwPaperSink** hold values necessary for connecting with COPaper to receive incoming notifications through the [**IPaperSink**](ipapersink-methods.md) interface.</span></span> <span data-ttu-id="7618d-112">Le membre **m \_ bDirty** contient un indicateur qui indique que l’utilisateur a modifié le dessin et qu’il ne reflète plus les données stockées dans son fichier.</span><span class="sxs-lookup"><span data-stu-id="7618d-112">Member **m\_bDirty** holds a flag indicating that the user has changed the drawing and that it no longer reflects the data stored in its file.</span></span>

<span data-ttu-id="7618d-113">Le membre **m \_ pIPaper** contient le pointeur d’interface principal vers l’objet du codocument.</span><span class="sxs-lookup"><span data-stu-id="7618d-113">Member **m\_pIPaper** holds the main interface pointer to the COPaper object.</span></span> <span data-ttu-id="7618d-114">Toutes les fonctionnalités du colivre sont accessibles via ce pointeur.</span><span class="sxs-lookup"><span data-stu-id="7618d-114">All of the COPaper functionality is accessed through this pointer.</span></span>

<span data-ttu-id="7618d-115">Le membre **m \_ nLockKey** est utilisé pour prendre en charge un modèle de verrouillage client qui est utilisé avec plusieurs clients pour permettre à un client d’accéder de façon exclusive à un objet de codocument partagé.</span><span class="sxs-lookup"><span data-stu-id="7618d-115">The **m\_nLockKey** member is used to support a client locking scheme that is used with multiple clients to allow a client exclusive access to a shared COPaper object.</span></span> <span data-ttu-id="7618d-116">Le codocument affecte **m \_ nLockKey** lors d’un appel [**IPaper**](ipaper-methods.md)::**Lock** et est transmis en tant que paramètre par le client lors d’appels ultérieurs au codocument.</span><span class="sxs-lookup"><span data-stu-id="7618d-116">COPaper assigns **m\_nLockKey** during an [**IPaper**](ipaper-methods.md)::**Lock** call and is passed as a parameter by the client in subsequent calls to COPaper.</span></span> <span data-ttu-id="7618d-117">Le colivreur effectue le travail dans ces appels uniquement si la clé de verrouillage transmise correspond à la dernière remise de la clé à un client par le biais du colivre.</span><span class="sxs-lookup"><span data-stu-id="7618d-117">COPaper will perform the work in those calls only if the lock key that is passed matches the key last handed out to a client by COPaper.</span></span>

<span data-ttu-id="7618d-118">Le membre **m \_ pPapFile** contient un pointeur vers un objet [**CPapFile**](cpapfile-class-and-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="7618d-118">Member **m\_pPapFile** holds a pointer to a [**CPapFile**](cpapfile-class-and-methods.md) object.</span></span> <span data-ttu-id="7618d-119">Il s’agit d’un objet C++ qui encapsule les opérations de chargement et d’enregistrement sur un fichier composé de stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="7618d-119">It is a C++ object that encapsulates load and save operations on a structured storage compound file.</span></span> <span data-ttu-id="7618d-120">**CPapFile** fonctionne avec l’objet du coarticle basé sur le serveur sous-jacent pour charger et enregistrer les données de dessin du plan.</span><span class="sxs-lookup"><span data-stu-id="7618d-120">**CPapFile** works with the underlying server-based COPaper object to load and save the COPaper drawing data.</span></span>

 

 




