---
title: IPaper enregistrer
description: Le principal objectif de cet exemple de code est de savoir comment le colivre peut charger et enregistrer ses données papier dans des fichiers composés. Les implémentations de la méthode IPaper, Load et Save sont décrites en détail.
ms.assetid: 62154658-ff47-425f-94da-ee2806de5318
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ea49f194e64ab3f0cfd78569b1e6ff9ddee577
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106545733"
---
# <a name="ipapersave"></a>IPaper :: enregistrer

Le principal objectif de cet exemple de code est de savoir comment le colivre peut charger et enregistrer ses données papier dans des fichiers composés. Les implémentations de la méthode [**IPaper**](ipaper-methods.md), [**Load**](ipaper--load.md)et **Save** sont décrites en détail.

Voici la méthode **IPaper :: Save** de Paper. cpp.


```C++
STDMETHODIMP COPaper::CImpIPaper::Save(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    ULONG ulToWrite, ulWritten;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
        // Use the COM service to mark this compound file as one 
        // that is handled by our server component, DllPaper.
        WriteClassStg(pIStorage, CLSID_DllPaper);

        // Use the COM Service to write user-readable clipboard 
        // format into the compound file.
        WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, 
                            TEXT(CLIPBDFMT_STR));

        // Create the stream to be used for the actual paper data.
        // Call it "PAPERDATA".
        hr = pIStorage->CreateStream(
               STREAM_PAPERDATA_USTR,
        STGM_CREATE | STGM_WRITE | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained a stream. Write data to it.
          // First, write PAPER_PROPERTIES structure.
          m_PaperProperties.lInkArraySize = m_lInkDataEnd+1;
          m_PaperProperties.crWinColor = m_crWinColor;
          m_PaperProperties.WinRect.right = m_WinRect.right;
          m_PaperProperties.WinRect.bottom = m_WinRect.bottom;
          ulToWrite = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Write(&m_Paper_Properties, ulToWrite, 
                               &ulWritten);
          if (SUCCEEDED(hr) && ulToWrite != ulWritten)
            hr = STG_E_CANTSAVE;
          if (SUCCEEDED(hr))
          {
            // Now, write the complete array of Ink Data.
            ulToWrite = m_PaperProperties.lInkArraySize * 
                                                     sizeof(INKDATA);
            hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
            if (SUCCEEDED(hr) && ulToWrite != ulWritten)
              hr = STG_E_CANTSAVE;
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify all other connected clients that Paper is now saved.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_SAVED, 0, 0, 0, 0);

    return hr;
  }
```



Dans cette relation de client et de serveur, le colivre ne crée pas le fichier composé utilisé pour stocker les données de papier. Pour les méthodes d' **enregistrement** et de [**chargement**](ipaper--load.md) , le client transmet un pointeur d’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pour un fichier composé existant. Il utilise ensuite l' **IStorage** pour écrire et lire des données dans ce fichier composé. Dans **IPaper :: Save** ci-dessus, plusieurs types de données sont stockés.

Le CLSID de DllPaper, CLSID \_ DllPaper, est sérialisé et stocké dans un flux spécial contrôlé par com au sein de l’objet de stockage appelé « \\ 001CompObj ». La fonction de service [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) effectue ce stockage. Ces données de CLSID stockées peuvent être utilisées pour associer le contenu de stockage au composant DllPaper qui a été créé et peut l’interpréter. Dans cet exemple, le stockage racine est passé par **StoClien** et, par conséquent, le fichier composé entier est associé au composant DllPaper. Ces données CLSID peuvent être récupérées ultérieurement à l’aide d’un appel à la fonction de service [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) .

Étant donné que DllPaper traite les données modifiables, il est également approprié d’enregistrer un format de presse-papiers dans le stockage. La fonction de service [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) est appelée pour stocker une désignation de format de presse-papiers et un nom lisible par l’utilisateur pour le format. Le nom lisible par l’utilisateur est destiné à l’affichage de l’interface graphique dans les listes de sélection. Le nom passé ci-dessus utilise une macro, CLIPBDFMT \_ Str, qui est définie comme « DllPaper 1,0 » dans Paper. h. Ces données stockées dans le presse-papiers peuvent être récupérées ultérieurement à l’aide d’un appel à la fonction de service [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg). Cette fonction retourne une valeur de chaîne allouée à l’aide de l’allocateur de mémoire de tâche. L’appelant est responsable de la libération de la chaîne.

**Save** Next crée un flux dans le stockage pour les données du livre blanc. Le flux est appelé « PAPERDATA » et est passé à l’aide de la \_ macro PAPERDATA de flux \_ USTR. La méthode [**IStorage :: CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) requiert que cette chaîne soit au format Unicode. Étant donné que la chaîne est fixe au moment de la compilation, la macro est définie en tant que Unicode dans Paper. h.

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

Le’L’avant la chaîne, indiquant LONG, y parvient.

La méthode [**CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) crée et ouvre un flux dans le stockage spécifié. Un pointeur d’interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pour le nouveau flux est passé dans une variable de pointeur d’interface appelant. AddRef est appelé sur ce pointeur d’interface dans **CreateStream,**, et l’appelant doit libérer ce pointeur après l’avoir utilisé. La méthode **CreateStream,** reçoit de nombreux indicateurs de mode d’accès, comme suit.

STGM \_ Create \| STGM \_ Write \| STGM \_ direct \| STGM \_ share \_ exclusive

[**STGM \_ CRÉER**](stgm-constants.md) crée un flux ou remplace un nouveau flux existant du même nom. [**STGM \_ WRITE**](stgm-constants.md) ouvre le flux avec l’autorisation Write. [**STGM \_ DIRECT**](stgm-constants.md) ouvre le flux pour l’accès direct, par opposition à l’accès transactionnel. [**STGM \_ PARTAGER \_ exclusive**](stgm-constants.md) ouvre le fichier pour une utilisation exclusive, non partagée par l’appelant.

Une fois le flux PAPERDATA correctement créé, l’interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) est utilisée pour écrire dans le flux. La méthode **IStream :: Write** est utilisée pour stocker le contenu de la structure de \_ Propriétés Paper. Il s’agit essentiellement d’un en-tête de propriétés au début du flux. Étant donné que le numéro de version est la première chose dans le fichier, il peut être lu indépendamment pour déterminer comment traiter les données qui suivent. Si la quantité de données réellement écrites n’est pas égale à la quantité demandée, la méthode Save est abandonnée et retourne STG \_ E \_ CANTSAVE.

L’enregistrement de la totalité du tableau de données manuscrites dans le flux est simple.


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



Étant donné que la méthode [**IStream :: Write**](/windows/desktop/api/Objidl/nn-objidl-istream) opère sur un tableau d’octets, le nombre d’octets de données d’encre stockées dans le tableau est calculé et l’opération d’écriture commence au début du tableau. Si la quantité de données réellement écrites n’est pas égale à la quantité demandée, la méthode **Save** retourne STG \_ E \_ CANTSAVE.

Une fois le flux écrit, la méthode **IPaper :: Save** libère le pointeur [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) qu’il utilisait.

La méthode **Save** appelle également le client [**IPaperSink**](ipapersink-methods.md) (dans la méthode Internal NotifySinks) pour notifier au client que l’opération d’enregistrement est terminée. À ce stade, la méthode **Save** retourne au client appelant, qui libère généralement le pointeur [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .

 

 




