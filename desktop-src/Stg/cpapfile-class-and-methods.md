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
# <a name="cpapfile-class-and-methods"></a>Classe et méthodes CPapFile

**StoClien** encapsule ses opérations de fichiers composés dans un objet C++ CPapFile.

Voici la déclaration de la classe **CPapFile** à partir de Papfile. h.


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



L’objet CPapFile conserve un nom de fichier actuel dans le membre **m \_ szCurFileName**. Ce nom de fichier est utilisé comme valeur par défaut dans les méthodes [**Load**](load-method---cpapfile.md) et [**Save**](save-method---cpapfile.md) s’ils ne reçoivent pas explicitement un nom de fichier.

Le membre **m \_ pIPaper** conserve un pointeur d’interface vers l’interface [**IPaper**](ipaper-methods.md) du colivre. Le membre **m \_ pIStorage** conserve un pointeur vers l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pour le fichier composite actuel que **StoClien** utilise pour le stockage structuré.

Voici un résumé des méthodes de CPapFile.


```C++
HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
    // Initializes CPapFile.

  HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
    // Loads default or specified paper data file.

  HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);
    // Saves drawing data to the current paper data file or
    // to a specified paper data file.
```



 

 




