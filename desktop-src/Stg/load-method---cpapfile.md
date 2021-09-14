---
title: Load, méthode-CPapFile
description: Une fois ces opérations réussies, l’interface IStorage obtenue est libérée. Cela ferme le fichier et indique que le fichier n’est pas ouvert pendant d’autres opérations du client. Il sera rouvert à la demande.
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- Load, méthode-CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe70be7241fe1e1eaeb779317e11a76fb479f76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008917"
---
# <a name="load-method---cpapfile"></a>Load, méthode-CPapFile

Une fois ces opérations réussies, l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) obtenue est libérée. Cela ferme le fichier et indique que le fichier n’est pas ouvert pendant d’autres opérations du client. Il sera rouvert à la demande.

Cet exemple est la méthode de **chargement** **CPapFile** à partir de Papfile. cpp.


```C++
HRESULT CPapFile::Load(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If null file name passed then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Verify that the file is using the APPUTIL function.
    if (FileExist(pszFile))
    {
      // Use the COM service to verify that the file is actually a 
      // valid compound file.
      hr = StgIsStorageFile(pszFile);
      if (SUCCEEDED(hr))
      {
        // Use the COM service to open the compound file and
        // obtain an IStorage interface.
        hr = StgOpenStorage(
               pszFile,
               NULL,
               STGM_DIRECT | STGM_READ | STGM_SHARE_EXCLUSIVE,
               NULL,
               0,
               &m_pIStorage);
        if (SUCCEEDED(hr))
        {
          // An IStorage interface has been obtained. Now, request 
          // the COPaper object on the server side to load into  
          // itself the file's paper data using IStorage for our 
          // client-provided compound file.
          hr = m_pIPaper->Load(nLockKey, m_pIStorage);
          if (SUCCEEDED(hr))
          {
            // The paper data was loaded and a current compound
            // file name exists. Copy it for later use in a saves 
            // and loads.
            if (bNewFile)
              StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
          }

          // The Storage object is not required now. Do not hold the 
          // file open. Re-obtain the IStorage again later, when 
          // required (and thus re-open the compound file) for
          // another save or load.
          RELEASE_INTERFACE(m_pIStorage);
        }
      }
    }

    return (hr);
  }
  
```



### <a name="remarks"></a>Remarques

Comme avec la méthode [**Save**](save-method---cpapfile.md) , si la **valeur null** est transmise pour le paramètre *pszFileName* , le contenu stocké du membre **m \_ szCurFileName** est utilisé pour le nom de fichier. Étant donné qu’un fichier existant peut être ouvert, la fonction APPUTIL **FileExist** est d’abord utilisée pour vérifier que le fichier existe. S’il existe, la fonction de service [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) standard est appelée pour vérifier le format du fichier afin de déterminer s’il s’agit d’un fichier composé valide.

Si le fichier est valide, la fonction de service [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) standard est appelée pour ouvrir le fichier et retourner un pointeur vers une interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pour celui-ci.

Le premier paramètre est le nom du fichier composé à ouvrir. Comme avec l’appel [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) , cette chaîne est attendue dans le formulaire Unicode, et au cours de la compilation ANSI, une macro apputil est utilisée pour garantir que le paramètre ANSI est converti au format Unicode attendu.

Le deuxième paramètre de stockage prioritaire a la **valeur null**, ce qui signifie qu’il n’est pas utilisé dans cet exemple.

Les indicateurs du mode d’accès sont passés comme troisième paramètre pour spécifier les modes d’accès autorisés sur le fichier ouvert. [**STGM \_ LIRE**](stgm-constants.md) ouvre le fichier avec l’autorisation lecture seule. [**STGM \_ DIRECT**](stgm-constants.md) ouvre le fichier pour un accès direct, par opposition à l’accès transactionnel. [**STGM \_ PARTAGER \_ exclusive**](stgm-constants.md) ouvre le fichier pour une utilisation exclusive, non partagée par l’appelant.

Quatrième élément d’exclusion de la **valeur null**, indiquant qu’il n’est pas utilisé dans cet exemple.

Le cinquième paramètre est réservé pour une utilisation ultérieure et doit être égal à zéro.

L’adresse de la variable pointeur **m \_ pIStorage** est passée comme sixième paramètre. Lorsque l’appel est retourné avec succès, **m \_ pIStorage** contient un pointeur vers une interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Il s’agit de l’interface utilisée pour les opérations suivantes sur le fichier ouvert.

Dans ce cas, l’opération importante consiste à faire en sorte que l’objet du codocument charge ses données de dessin à partir du fichier. Pour ce faire, vous utilisez la méthode **Load** de l’interface [**IPaper**](ipaper-methods.md) du codocument. Si le « coarticle » parvient à charger ses données à l’aide de la [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) fournie, le nom du fichier composé est copié dans **m \_ szCurFileName** comme nouveau nom de fichier actuel.

Lorsque ces opérations sont terminées avec succès, l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) obtenue est libérée. Cela ferme le fichier et signifie que le fichier n’est pas ouvert pendant d’autres opérations du client. Il sera rouvert à la demande.

 

 




