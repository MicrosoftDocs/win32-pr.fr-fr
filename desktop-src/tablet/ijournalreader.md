---
description: fournit un accès en lecture à un fichier Journal Windows, en retournant un flux contenant une version XML du contenu du fichier.
ms.assetid: e4e19f69-6377-4f06-856d-7f9b453e7656
title: Interface IJournalReader (Journal. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: ff0151432e38a3e611e09efe2d5192eefb8c1d3e6cb0e79296e992b728c5a16a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590311"
---
# <a name="ijournalreader-interface"></a>Interface IJournalReader

fournit un accès en lecture à un fichier Journal Windows, en retournant un flux contenant une version XML du contenu du fichier.

> [!Note]  
> le composant de lecture du journal ne peut pas lire les fichiers journaux Windows créés par des ordinateurs exécutant Windows 7 ou une version ultérieure. L’interface IJournalReader doit être considérée comme dépréciée ou obsolète et ne doit pas être utilisée.

 

## <a name="members"></a>Membres

L’interface **IJournalReader** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IJournalReader** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IJournalReader** possède ces méthodes.



| Méthode                                                  | Description                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**ReadFromStream**](ijournalreader-readfromstream.md) | Prend un flux dans un fichier de note du journal et retourne un flux de données XML représentant le contenu du document.<br/> |



 

## <a name="remarks"></a>Remarques

La classe **JournalReader** vous permet de charger un flux de document de journal et de recevoir un flux XML représentant le contenu. Vous pouvez reconstituer, afficher et manipuler l’encre.

## <a name="examples"></a>Exemples

L’exemple suivant d’un gestionnaire pour l’événement [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) d’un bouton crée une instance de la classe **JournalReader** et l’utilise pour lire un fichier journal existant.

> [!Note]  
> La méthode **DisplayXml** appelée depuis cet exemple n’est pas affichée. L’implémentation spécifique d’une telle méthode dépend des besoins de votre application.

 


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  static TCHAR BASED_CODE szFilter[] = 
    _T("Journal files (*.jnt)|*.jnt|All files (*.*)|*.*");
  CFileDialog* fileDialog = new CFileDialog(TRUE, _T("*.jnt"), NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user via a File Open dialog
  if (fileDialog != NULL &&
      fileDialog->DoModal() == IDOK)
  {
    CString strFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(strFileName,
                              GENERIC_READ,
                              FILE_SHARE_READ,
                              NULL,
                              OPEN_EXISTING,
                              FILE_ATTRIBUTE_NORMAL,
                              NULL);
    
    if (hFile != INVALID_HANDLE_VALUE)
    {
      // Allocate memory to hold the file contents
      DWORD dwFileSize = GetFileSize(hFile, NULL);
      HGLOBAL hGlobal = GlobalAlloc(GHND, dwFileSize);

      if (hGlobal != NULL)
      {
        LPBYTE pData = (LPBYTE)GlobalLock(hGlobal);

        if (pData != NULL)
        {
          DWORD dwRead;

          // Read the Journal file into the pData buffer
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) &&
              (dwRead == dwFileSize))
          {
            HRESULT hr;
            IStream* pJntStream;

            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              IJournalReader* pJntReader;

              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                IStream* pXmlStream;

                // Read in the JNT file via the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                if (SUCCEEDED(hr))
                {
                  // Display results
                  DisplayXml(pXmlStream);

                  // Clean up
                  pXmlStream->Release();
                }
                pJntReader->Release();
              }
              pJntStream->Release();
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
      CloseHandle(hFile);
    }
    delete fileDialog;
  }
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                         |
| En-tête<br/>                   | <dl> <dt>Journal. h (nécessite également le journal \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[GUID de propriété personnalisée](custom-property-guids.md)
</dt> <dt>

[**Méthode ReadFromStream**](ijournalreader-readfromstream.md)
</dt> </dl>

 

