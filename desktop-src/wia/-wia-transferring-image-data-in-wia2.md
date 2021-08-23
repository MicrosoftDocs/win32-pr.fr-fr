---
description: étant donné que le transfert de données d’image est basé sur la diffusion en continu dans Windows acquisition d’images (WIA) 2,0, vous n’avez pas besoin de spécifier un type de destination (par exemple,
ms.assetid: ebb9fce5-9450-4ffe-b480-b21670b60f90
title: Transfert de données d’image dans WIA 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66aca2179c477f49bc76197795ddf9d59792ca242da8729c169c39aa69553161
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592959"
---
# <a name="transferring-image-data-in-wia-20"></a>Transfert de données d’image dans WIA 2,0

> [!Note]  
> ce didacticiel montre comment transférer des données d’image dans des applications qui s’exécutent sur Windows Vista ou version ultérieure. pour plus d’informations sur le transfert de données d’image dans les applications qui s’exécutent sur Windows XP ou version antérieure, consultez [transfert de données d’image dans WIA 1,0](-wia-transferring-image-data.md) .

 

étant donné que le transfert de données d’image est basé sur la diffusion en continu dans Windows acquisition d’images (WIA) 2,0, vous n’avez pas besoin de spécifier un type de destination (par exemple, mémoire ou fichier). L’application donne simplement à WIA 2,0 le flux à utiliser et le pilote lit ou écrit dans le flux. Le flux peut être un flux de fichier, un flux de mémoire ou tout autre type de flux, et est transparent pour le pilote. L’utilisation de flux offre également une intégration facile avec le filtre de traitement d’image.

Utilisez les méthodes de l’interface [**IWiaTransfer**](-wia-iwiatransfer.md) pour transférer des données d’un appareil WIA 2,0 vers une application. Cette interface est disponible via l’interface [**IWiaItem2**](-wia-iwiaitem2.md) . L’interface **IWiaTransfer** a des méthodes pour demander le chargement ou le téléchargement de données vers et à partir d’un appareil. Ces méthodes prennent un rappel fourni par l’application et utilisent un [IStream](/windows/win32/api/objidl/nn-objidl-istream) fourni par l’application pour la destination réelle du transfert de données.

Les applications doivent interroger un élément image pour obtenir un pointeur vers son interface [**IWiaTransfer**](-wia-iwiatransfer.md) , comme illustré dans l’exemple de code suivant :


```
    // Get the IWiaTransfer interface
    //
    IWiaTransfer *pWiaTransfer = NULL;
    hr = pIWiaItem2->QueryInterface(IID_IWiaTransfer,(void**)&pWiaTransfer);
```



Dans le code précédent, nous supposons que **pWiaItem2** est un pointeur valide vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) . L’appel à [IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) remplit **pWiaTransfer** avec un pointeur vers l’interface [**IWiaTransfer**](-wia-iwiatransfer.md) de l’élément référencé par **pWiaItem2**.

L’application instancie ensuite l’objet de rappel, comme indiqué ici.


```
    //   Instantiate the object which receives the callbacks
    //
    CWiaTransferCallback *pWiaClassCallback = new CWiaTransferCallback;
```



L’application définit ensuite les propriétés à l’aide de l’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) de l’élément [**IWiaItem2**](-wia-iwiaitem2.md) et effectue le transfert.

Téléchargement :


```
    // Download   
    hr = pWiaTransfer->Download(0,pWiaClassCallback);
```



Téléchargement


```
    //Create child item which eventually will be the uploaded image 
    IWiaItem2* pWiaItemChild = NULL;
    HRESULT hr = pIWiaItem2->CreateChildItem(WiaItemTypeImage|WiaItemTypeFile,0,bzUploadFileName,&pWiaItemChild);
    
    if(SUCCEEDED(hr))
    {
                
        //Set the format for the child item as BMP 
        IWiaPropertyStorage* pWiaChildPropertyStorage = NULL;
        hr = pWiaItemChild->QueryInterface( IID_IWiaPropertyStorage, (void**)&pWiaChildPropertyStorage );
        if(SUCCEEDED(hr))
        {
            WritePropertyGuid(pWiaChildPropertyStorage,WIA_IPA_FORMAT,WiaImgFmt_BMP );

            //release pWiaChildPropertyStorage
            pWiaChildPropertyStorage->Release();
            pWiaChildPropertyStorage = NULL;
        }
        

        //Get the IWiaTransfer interface of the child
        IWiaTransfer* pWiaTransferChild = NULL;
        hr = pWiaItemChild->QueryInterface( IID_IWiaTransfer, (void**)&pWiaTransferChild );
        if(SUCCEEDED(hr)){
            IStream* pUploadStream = NULL;
                                        
            //Create stream on test.BMP file
            hr = SHCreateStreamOnFile(L"test.BMP",STGM_READ, &pUploadStream);
            if(SUCCEEDED(hr)){
                pWiaTransferChild->Upload(0,pUploadStream,pWiaClassCallback);
                
            }
         }
   
      }
```



Voici l’exemple complet de transfert de données :


```
HRESULT TransferWiaItem( IWiaItem2 *pIWiaItem2)
{
    // Validate arguments
    if (NULL == pIWiaItem2)
    {
        _tprintf(TEXT("\nInvalid parameters passed"));
        return E_INVALIDARG;
    }
    
    // Get the IWiaTransfer interface
    IWiaTransfer *pWiaTransfer = NULL;
    HRESULT hr = pIWiaItem2->QueryInterface( IID_IWiaTransfer, (void**)&pWiaTransfer );
    if (SUCCEEDED(hr))
    {
        // Create our callback class
        CWiaTransferCallback *pWiaClassCallback = new CWiaTransferCallback;
        if (pWiaClassCallback)
        {
            
              LONG lItemType = 0;
              hr = pIWiaItem2->GetItemType( &lItemType );

              //download all items which have WiaItemTypeTransfer flag set
              if(lItemType & WiaItemTypeTransfer)
              {

                  // If it is a folder, do folder download . Hence with one API call, all the leaf nodes of this folder 
                  // will be transferred
                  if ((lItemType & WiaItemTypeFolder))
                  {
                        _tprintf ( L"\nI am a folder item");
                        hr = pWiaTransfer->Download(WIA_TRANSFER_ACQUIRE_CHILDREN, pWiaClassCallback);
                        if(S_OK == hr)
                        {
                            _tprintf(TEXT("\npWiaTransfer->Download() on folder item SUCCEEDED"));
                        }
                        else if(S_FALSE == hr)
                        {
                            ReportError(TEXT("\npWiaTransfer->Download() on folder item returned S_FALSE. Folder may not be having child items"),hr);
                        }
                        else if(FAILED(hr))
                        {
                            ReportError(TEXT("\npWiaTransfer->Download() on folder item failed"),hr);
                        }
                   }

                  
                  // If this is an file type, do file download
                  else if (lItemType & WiaItemTypeFile )
                  {
                      hr = pWiaTransfer->Download(0,pWiaClassCallback);
                      if(S_OK == hr)
                      {
                          _tprintf(TEXT("\npWiaTransfer->Download() on file item SUCCEEDED"));
                      }
                      else if(S_FALSE == hr)
                      {
                          ReportError(TEXT("\npWiaTransfer->Download() on file item returned S_FALSE. File may be empty"),hr);
                      }
                      else if(FAILED(hr))
                      {
                         ReportError(TEXT("\npWiaTransfer->Download() on file item failed"),hr);
                      }
                  }                     
                }
                
                // Release our callback.  It should now delete itself.
                pWiaClassCallback->Release();
                pWiaClassCallback = NULL;
        }
        else
        {
            ReportError( TEXT("\nUnable to create CWiaTransferCallback class instance") );
        }
            
        // Release the IWiaTransfer
        pWiaTransfer->Release();
        pWiaTransfer = NULL;
    }
    else
    {
        ReportError( TEXT("\npIWiaItem2->QueryInterface failed on IID_IWiaTransfer"), hr );
    }
    return hr;
}

// Callback Class should be something like this:

class CWiaTransferCallback : public IWiaTransferCallback
{
public: // Constructors, destructor
    CWiaTransferCallback () : m_cRef(1) {};
    ~ CWiaTransferCallback () {};

public: // IWiaTransferCallback
    HRESULT __stdcall TransferCallback(
        LONG                lFlags,
        WiaTransferParams   *pWiaTransferParams)
    {
        HRESULT hr = S_OK;

        switch (pWiaTransferParams->lMessage)
        {
            case WIA_TRANSFER_MSG_STATUS:
                ...
                break;
            case WIA_TRANSFER_MSG_END_OF_STREAM:
                ...
                break;
            case WIA_TRANSFER_MSG_END_OF_TRANSFER:
                ...
                break;
            default:
                break;
        }

        return hr;
    }

    HRESULT __stdcall GetNextStream(
        LONG    lFlags,
        BSTR    bstrItemName,
        BSTR    bstrFullItemName,
        IStream **ppDestination)
    {

        HRESULT hr = S_OK;

        //  Return a new stream for this item's data.
        //
        hr = CreateDestinationStream(bstrItemName, ppDestination);
        return hr;
    }

public: // IUnknown
        .
        .
        . // Etc.

private:
    /// For ref counting implementation
    LONG                m_cRef;
};

```



 

 
