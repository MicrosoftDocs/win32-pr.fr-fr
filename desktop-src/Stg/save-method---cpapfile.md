---
title: Save, méthode-CPapFile
description: Lorsque CPapFile est initialisé, il peut être utilisé pour enregistrer les données de dessin actuelles contenues dans l’objet du colivre.
ms.assetid: ceac32e5-7d47-480b-b1cd-5a17ac04dd0c
keywords:
- Save, méthode-CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3166b649f28cb1a8ddc37e9efc53465a6cb5d3e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940342"
---
# <a name="save-method---cpapfile"></a>Save, méthode-CPapFile

Lorsque **CPapFile** est initialisé, il peut être utilisé pour enregistrer les données de dessin actuelles contenues dans l’objet du colivre.

## <a name="save-method-papfilecpp"></a>Méthode Save (PAPFILE. COTISATIONS

Cet exemple est la méthode **CPapFile** [**Save**](ipaper--save.md) de Papfile. cpp.


```C++
HRESULT CPapFile::Save(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If a null file name is passed, then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Use the COM service to reopen, or create, the compound file.
    hr = StgCreateDocfile(
        pszFile,
    STGM_CREATE | STGM_DIRECT | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0,
        &m_pIStorage);
    if (SUCCEEDED(hr))
    {
      // Obtained the IStorage. The compound file is open.
      // Instruct the COPaper object on the server side to save its
      // paper data into the compound file using the IStorage of our
      // client-provided compound file.
      hr = m_pIPaper->Save(nLockKey, m_pIStorage);
      if (SUCCEEDED(hr))
      {
        // The paper data was saved and obtained a new current 
        // compound file name. Copy it for later use in saves 
        // and loads.
        if (bNewFile)
          StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
      }

      // Storage complete. Do not hold the file open.
      // Re-obtain the IStorage again later (and thus re-open
      // the compound file) when required for another save or load.
      RELEASE_INTERFACE(m_pIStorage);
    }

    return (hr);
  }
  
```



Si la **valeur null** est transmise pour le paramètre *pszFileName* , le contenu stocké du membre **m \_ szCurFileName** est utilisé pour le nom de fichier. Le *nLockKey* est la clé de verrouillage du client obtenue dans un appel précédent à la méthode de [**verrouillage**](ipaper-methods.md) du copapier dans l’interface **IPaper** .

La fonction de service [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) standard com est appelée pour créer le fichier composé dans lequel les données de dessin seront enregistrées.

Le nom du fichier composé à créer est passé en tant que premier paramètre. Cela est attendu par [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) comme une chaîne Unicode. Quand **StoClien** est compilé pour des chaînes ANSI (Unicode n’est pas défini, qui est la valeur par défaut dans le Makefile), cet appel réduit en fait un appel à une fonction apputil interne, **\_ StgCreateDocFile**. Cette fonction effectue la conversion appropriée du paramètre ANSI pszFile en une version Unicode avant d’appeler **StgCreateDocFile**. Pour plus d’informations, consultez apputil. h et Stoserve.htm.

Les indicateurs du mode d’accès sont passés comme deuxième paramètre et déterminent les modes d’accès autorisés sur le nouveau fichier. L’indicateur [STGM \_ Create](stgm-constants.md) Access mode crée un nouveau fichier composé ou remplace un fichier existant du même nom. [STGM \_ READWRITE](stgm-constants.md) ouvre le fichier avec l’autorisation de lecture-écriture. [STGM \_ DIRECT](stgm-constants.md) ouvre le fichier pour un accès direct, par opposition à l’accès transactionnel. [STGM \_ PARTAGER \_ exclusive](stgm-constants.md) ouvre le fichier pour une utilisation exclusive, non partagée par l’appelant.

Le troisième paramètre est réservé et doit être égal à zéro.

L’adresse de la variable pointeur **m \_ pIStorage** est transmise à [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) en tant que quatrième paramètre. Lorsque l’appel est retourné avec succès, **m \_ pIStorage** contient un pointeur d’interface vers une interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Il s’agit de l’interface utilisée pour les opérations suivantes sur le fichier.

Dans ce cas, l’opération importante consiste à faire en sorte que l’objet du colivre stocke ses données de dessin dans le fichier. Pour ce faire, vous utilisez la méthode [**Save**](ipaper--save.md) de l’interface [**IPaper**](ipaper-methods.md) du colivre. Si l’enregistrement de ses données dans l’objet de stockage fourni par le colivre fonctionne, le nom du fichier composé est copié dans **m \_ szCurFileName** comme nouveau nom de fichier actuel.

 

 




