---
description: Prend un flux dans un fichier de note du journal et retourne un flux de données XML représentant le contenu du document.
ms.assetid: 5a169dfe-b102-4aef-9efe-5db2cd2fb96f
title: 'IJournalReader :: ReadFromStream, méthode (Journal. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader.ReadFromStream
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 258ac30b8857fa4ef24bd86a08c7e402229f4bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540816"
---
# <a name="ijournalreaderreadfromstream-method"></a>IJournalReader :: ReadFromStream, méthode

Prend un flux dans un fichier de note du journal et retourne un flux de données XML représentant le contenu du document.

> [!Note]  
> Le composant de lecture du journal ne peut pas lire les fichiers journaux Windows créés par des ordinateurs exécutant Windows 7 ou une version ultérieure. L’interface IJournalReader doit être considérée comme dépréciée ou obsolète et ne doit pas être utilisée.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pJournalFileStream* \[ dans\]
</dt> <dd>

Objet [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) représentant le fichier journal à lire.

</dd> <dt>

*ppXmlStream* \[ out, retval\]
</dt> <dd>

Pointeur vers l’adresse d’un objet [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) qui recevra le flux XML créé par la lecture du fichier journal.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Les flux sont utilisés pour éviter l’accès direct au système de fichiers et pour permettre le choix de la méthode d’analyse XML à utiliser.

## <a name="examples"></a>Exemples

L’exemple suivant d’un gestionnaire pour l’événement [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) d’un bouton crée une instance de l’interface d' [**interface IJournalReader**](ijournalreader.md) et l’utilise pour lire un fichier journal existant.


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  IStream* pJntStream;
  IStream* pXmlStream;
  IJournalReader* pJntReader;
  HRESULT hr;
  CString szFileName = "";
  static char BASED_CODE szFilter[] = 
    "Journal files (*.jnt)|*.jnt|All files (*.*)|*.*";
  CFileDialog* fileDialog = new CFileDialog(TRUE, "*.jnt", NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user by using a File Open dialog
  if (IDOK == fileDialog->DoModal())
  {
    szFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(szFileName.GetBuffer(), GENERIC_READ, FILE_SHARE_READ, NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    
    if (INVALID_HANDLE_VALUE != hFile)
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
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) && dwRead == dwFileSize)
          {
            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                // Read in the JNT file by using the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                // Display results
                if (SUCCEEDED(hr))
                {
                  DisplayXml(pXmlStream);
                }

                // Clean up
                pXmlStream->Release();
                pJntReader = NULL;
                pJntStream->Release();
              }
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
    }
  }
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                         |
| En-tête<br/>                   | <dl> <dt>Journal. h (nécessite également le journal \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IJournalReader**](ijournalreader.md)
</dt> <dt>

[Référence du schéma du lecteur de journal](journal-reader-schema-reference.md)
</dt> </dl>

 

