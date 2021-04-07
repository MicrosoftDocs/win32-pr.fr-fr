---
title: Classe et méthodes CPapFile
description: StoClien encapsule ses opérations de fichiers composés dans un objet C++ CPapFile.
ms.assetid: 21a3e170-0a73-4744-8cfc-3a04e0571792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa970aecf275afbf7bc5b6d68c69de3367e48aa5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939838"
---
# <a name="cpapfile-class-and-methods"></a><span data-ttu-id="1b067-103">Classe et méthodes CPapFile</span><span class="sxs-lookup"><span data-stu-id="1b067-103">CPapFile Class and Methods</span></span>

<span data-ttu-id="1b067-104">**StoClien** encapsule ses opérations de fichiers composés dans un objet C++ CPapFile.</span><span class="sxs-lookup"><span data-stu-id="1b067-104">**StoClien** encapsulates its compound file operations in a CPapFile C++ object.</span></span>

<span data-ttu-id="1b067-105">Voici la déclaration de la classe **CPapFile** à partir de Papfile. h.</span><span class="sxs-lookup"><span data-stu-id="1b067-105">The following is the **CPapFile** class declaration from Papfile.h.</span></span>


```C++
class CPapFile
  {
    public:
      CPapFile(void);
      ~CPapFile(void);
      HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
      HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
      HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);

    private:
      TCHAR          m_szCurFileName[MAX_PATH];
      IPaper*        m_pIPaper;
      IStorage*      m_pIStorage;
  };
  
```



<span data-ttu-id="1b067-106">L’objet CPapFile conserve un nom de fichier actuel dans le membre **m \_ szCurFileName**.</span><span class="sxs-lookup"><span data-stu-id="1b067-106">The CPapFile object keeps a current file name in member **m\_szCurFileName**.</span></span> <span data-ttu-id="1b067-107">Ce nom de fichier est utilisé comme valeur par défaut dans les méthodes [**Load**](load-method---cpapfile.md) et [**Save**](save-method---cpapfile.md) s’ils ne reçoivent pas explicitement un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="1b067-107">This file name is used as a default in the [**Load**](load-method---cpapfile.md) and [**Save**](save-method---cpapfile.md) methods when they do not explicitly receive a file name.</span></span>

<span data-ttu-id="1b067-108">Le membre **m \_ pIPaper** conserve un pointeur d’interface vers l’interface [**IPaper**](ipaper-methods.md) du colivre.</span><span class="sxs-lookup"><span data-stu-id="1b067-108">Member **m\_pIPaper** keeps an interface pointer to the COPaper [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="1b067-109">Le membre **m \_ pIStorage** conserve un pointeur vers l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pour le fichier composite actuel que **StoClien** utilise pour le stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="1b067-109">Member **m\_pIStorage** keeps a pointer to the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface for the current compound file that **StoClien** is using for structured storage.</span></span>

<span data-ttu-id="1b067-110">Voici un résumé des méthodes de CPapFile.</span><span class="sxs-lookup"><span data-stu-id="1b067-110">The following is a summary of CPapFile's methods.</span></span>


```C++
HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
    // Initializes CPapFile.

  HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
    // Loads default or specified paper data file.

  HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);
    // Saves drawing data to the current paper data file or
    // to a specified paper data file.
```



 

 




