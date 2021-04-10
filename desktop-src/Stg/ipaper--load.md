---
title: Charge IPaper
description: L’exemple de code C++ suivant montre comment ouvrir le flux existant dans le stockage, lire les nouvelles propriétés de papier dans, puis les définir comme valeurs actuelles pour le codocument.
ms.assetid: a1559d97-387f-4d1a-8a9d-fa5c27abd545
keywords:
- Charge IPaper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b5f16b8fe649d08226b2cff5a4b1a5234bddb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940200"
---
# <a name="ipaperload"></a>IPaper :: Load

L’exemple de code C++ suivant montre comment ouvrir le flux existant dans le stockage, lire les nouvelles propriétés de papier dans, puis les définir comme valeurs actuelles pour le codocument.

Voici la méthode **IPaper :: Load** de Paper. cpp.


```
STDMETHODIMP COPaper::CImpIPaper::Load(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    INKDATA* paInkData;
    ULONG ulToRead, ulReadIn;
    LONG lNewArraySize;
    PAPER_PROPERTIES NewProps;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
       // Open the "PAPERDATA" stream where the paper data is stored.
        hr = pIStorage->OpenStream(
               STREAM_PAPERDATA_USTR,
               0,
               STGM_READ | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained paper data stream. Read the Paper Properties.
          ulToRead = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Read(
                           &NewProps,
                           ulToRead,
                           &ulReadIn);
          if (SUCCEEDED(hr) && ulToRead != ulReadIn)
            hr = E_FAIL;
          if (SUCCEEDED(hr))
          {
            // Handle the different versions of ink data format.
            switch (NewProps.lInkDataVersion)
            {
              case INKDATA_VERSION10:
                // Allocate an ample-sized ink data array.
                lNewArraySize = NewProps.lInkArraySize + 
                                               INKDATA_ALLOC;
                paInkData = new INKDATA[(LONG) lNewArraySize];
                if (NULL != paInkData)
                {
                  // Delete the old ink data array.
                  delete [] m_paInkData;

                  // Assign the new array.
                  m_paInkData = paInkData;
                  m_lInkDataMax = lNewArraySize;

                  // Read the complete array of Ink Data.
                  ulToRead = NewProps.lInkArraySize * sizeof(INKDATA);
                  hr = pIStream->Read(m_paInkData, 
                                      ulToRead, &ulReadIn);
                  if (SUCCEEDED(hr) && ulToRead != ulReadIn)
                    hr = E_FAIL;
                  if (SUCCEEDED(hr))
                  {
                    // Set COPaper to use the new PAPER_PROPERTIES
                    // data.
                    m_lInkDataEnd = NewProps.lInkArraySize-1;
                    m_crWinColor = NewProps.crWinColor;
                    m_WinRect.right = NewProps.WinRect.right;
                    m_WinRect.bottom = NewProps.WinRect.bottom;

                    // Copy the new properties into current 
                    // properties.
                    memcpy(
                      &m_PaperProperties,
                      &NewProps,
                      sizeof(PAPER_PROPERTIES));
                  }
                }
                else
                  hr = E_OUTOFMEMORY;
                break;
              default:
                hr = E_FAIL;  // Bad version.
                break;
            }
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify other connected clients that Paper is now loaded.
    // If Paper not loaded, then erase to a safe, empty ink data 
    // array.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_LOADED, 0, 0, 0, 0);
    else
      Erase(nLockKey);

    return hr;
  }
```



À présent, la méthode [**IStorage :: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) est appelée pour ouvrir le flux existant dans le stockage appelé « PAPERDATA ». Les indicateurs de mode d’accès sont pour l’accès en lecture seule, direct et non partagé. Lorsque le flux est ouvert, la méthode [**IStream :: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) est appelée pour lire la \_ structure de propriétés Paper. Si la quantité réellement lue n’est pas égale à la quantité demandée, l’opération de chargement est abandonnée et E \_ Fail est retourné. Si la version de format dans les propriétés de papier récemment lues \_ n’est pas reconnue, l’opération de chargement est abandonnée et la **charge** retourne E \_ Fail.

Avec une version de format de données manuscrites valide, la taille du nouveau tableau de données manuscrites à partir des propriétés de papier \_ qui a été lue est utilisée pour allouer un nouveau tableau de données d’encre de la taille requise. Les données d’encre existantes sont supprimées et ses données sont perdues. Si ces données étaient précieuses, elles devaient avoir été enregistrées avant l’appel de **Load** . Une fois le nouveau tableau alloué, [**IStream :: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) est rappelé pour lire les données dans le tableau à partir du flux. Si cet appel a échoué, les valeurs des propriétés du papier récemment lues sont adoptées comme valeurs actuelles pour le codocument.

Au cours de cette opération de chargement, une structure de propriétés de papier temporaire \_ , NewProps, a été utilisée pour contenir les nouvelles propriétés lues dans. Si tout se déroule correctement avec la charge, NewProps est copié dans la \_ structure des propriétés du papier, m \_ PaperProperties. Comme précédemment, une fois la charge terminée et l' [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) n’est plus nécessaire, le pointeur **IStream** est libéré.

En cas d’erreur à la fin de la **charge**, le tableau de données d’encre est effacé, car il contient peut-être des données endommagées.

S’il n’y a aucune erreur à la fin du **chargement**, la méthode cliente [**IPaperSink :: Loaded**](ipapersink-methods.md) est appelée, dans la méthode NotifySinks Internal, pour notifier au client que l’opération de chargement est terminée. Il s’agit d’une notification importante pour le client, car il doit afficher les nouvelles données d’encre chargées. Cette notification utilise de manière significative les fonctionnalités des objets connectables dans le codocument.

 

 




