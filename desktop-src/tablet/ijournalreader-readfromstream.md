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
# <a name="ijournalreaderreadfromstream-method"></a><span data-ttu-id="7f25e-103">IJournalReader :: ReadFromStream, méthode</span><span class="sxs-lookup"><span data-stu-id="7f25e-103">IJournalReader::ReadFromStream method</span></span>

<span data-ttu-id="7f25e-104">Prend un flux dans un fichier de note du journal et retourne un flux de données XML représentant le contenu du document.</span><span class="sxs-lookup"><span data-stu-id="7f25e-104">Takes a stream to a Journal Note file and returns an XML stream representing the contents of the document.</span></span>

> [!Note]  
> <span data-ttu-id="7f25e-105">Le composant de lecture du journal ne peut pas lire les fichiers journaux Windows créés par des ordinateurs exécutant Windows 7 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7f25e-105">The Journal Reader component cannot read Windows Journal files created by machines running Windows 7 or later.</span></span> <span data-ttu-id="7f25e-106">L’interface IJournalReader doit être considérée comme dépréciée ou obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="7f25e-106">The IJournalReader interface should be considered deprecated or obsolete and should not be used.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7f25e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f25e-107">Syntax</span></span>


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a><span data-ttu-id="7f25e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f25e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f25e-109">*pJournalFileStream* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f25e-109">*pJournalFileStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f25e-110">Objet [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) représentant le fichier journal à lire.</span><span class="sxs-lookup"><span data-stu-id="7f25e-110">An [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) object representing the Journal file to read.</span></span>

</dd> <dt>

<span data-ttu-id="7f25e-111">*ppXmlStream* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7f25e-111">*ppXmlStream* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7f25e-112">Pointeur vers l’adresse d’un objet [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) qui recevra le flux XML créé par la lecture du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="7f25e-112">A pointer to the address of an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) object that will receive the XML stream created by reading the Journal file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f25e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f25e-113">Return value</span></span>

<span data-ttu-id="7f25e-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7f25e-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7f25e-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7f25e-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f25e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7f25e-116">Remarks</span></span>

<span data-ttu-id="7f25e-117">Les flux sont utilisés pour éviter l’accès direct au système de fichiers et pour permettre le choix de la méthode d’analyse XML à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7f25e-117">Streams are used to avoid direct access to the file system and to allow choice in which XML parsing method to use.</span></span>

## <a name="examples"></a><span data-ttu-id="7f25e-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="7f25e-118">Examples</span></span>

<span data-ttu-id="7f25e-119">L’exemple suivant d’un gestionnaire pour l’événement [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) d’un bouton crée une instance de l’interface d' [**interface IJournalReader**](ijournalreader.md) et l’utilise pour lire un fichier journal existant.</span><span class="sxs-lookup"><span data-stu-id="7f25e-119">The following example of a handler for a button's [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event creates an instance of the [**IJournalReader Interface**](ijournalreader.md) interface and uses it to read an existing Journal file.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7f25e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f25e-120">Requirements</span></span>



| <span data-ttu-id="7f25e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f25e-121">Requirement</span></span> | <span data-ttu-id="7f25e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f25e-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f25e-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f25e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7f25e-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f25e-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7f25e-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f25e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7f25e-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f25e-126">None supported</span></span><br/>                                                                                         |
| <span data-ttu-id="7f25e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f25e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f25e-128"><dt>Journal. h (nécessite également le journal \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7f25e-128"><dt>Journal.h (also requires journal\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7f25e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7f25e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f25e-130"><dt>Journal.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f25e-130"><dt>Journal.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="7f25e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f25e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f25e-132">**Interface IJournalReader**</span><span class="sxs-lookup"><span data-stu-id="7f25e-132">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> <dt>

[<span data-ttu-id="7f25e-133">Référence du schéma du lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="7f25e-133">Journal Reader Schema Reference</span></span>](journal-reader-schema-reference.md)
</dt> </dl>

 

