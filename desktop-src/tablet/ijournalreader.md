---
description: Fournit un accès en lecture à un fichier journal Windows, en retournant un flux contenant une version XML du contenu du fichier.
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
ms.openlocfilehash: 7576996d341f13518879310f08c0a48996e1293f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320941"
---
# <a name="ijournalreader-interface"></a><span data-ttu-id="17452-103">Interface IJournalReader</span><span class="sxs-lookup"><span data-stu-id="17452-103">IJournalReader interface</span></span>

<span data-ttu-id="17452-104">Fournit un accès en lecture à un fichier journal Windows, en retournant un flux contenant une version XML du contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="17452-104">Provides read access to a Windows Journal file, returning a stream containing an XML version of the file's contents.</span></span>

> [!Note]  
> <span data-ttu-id="17452-105">Le composant de lecture du journal ne peut pas lire les fichiers journaux Windows créés par des ordinateurs exécutant Windows 7 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="17452-105">The Journal Reader component cannot read Windows Journal files created by machines running Windows 7 or later.</span></span> <span data-ttu-id="17452-106">L’interface IJournalReader doit être considérée comme dépréciée ou obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="17452-106">The IJournalReader interface should be considered deprecated or obsolete and should not be used.</span></span>

 

## <a name="members"></a><span data-ttu-id="17452-107">Membres</span><span class="sxs-lookup"><span data-stu-id="17452-107">Members</span></span>

<span data-ttu-id="17452-108">L’interface **IJournalReader** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="17452-108">The **IJournalReader** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="17452-109">**IJournalReader** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="17452-109">**IJournalReader** also has these types of members:</span></span>

-   [<span data-ttu-id="17452-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="17452-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="17452-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="17452-111">Methods</span></span>

<span data-ttu-id="17452-112">L’interface **IJournalReader** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="17452-112">The **IJournalReader** interface has these methods.</span></span>



| <span data-ttu-id="17452-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="17452-113">Method</span></span>                                                  | <span data-ttu-id="17452-114">Description</span><span class="sxs-lookup"><span data-stu-id="17452-114">Description</span></span>                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17452-115">**ReadFromStream**</span><span class="sxs-lookup"><span data-stu-id="17452-115">**ReadFromStream**</span></span>](ijournalreader-readfromstream.md) | <span data-ttu-id="17452-116">Prend un flux dans un fichier de note du journal et retourne un flux de données XML représentant le contenu du document.</span><span class="sxs-lookup"><span data-stu-id="17452-116">Takes a stream to a Journal Note file and returns an XML stream representing the contents of the document.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="17452-117">Notes</span><span class="sxs-lookup"><span data-stu-id="17452-117">Remarks</span></span>

<span data-ttu-id="17452-118">La classe **JournalReader** vous permet de charger un flux de document de journal et de recevoir un flux XML représentant le contenu.</span><span class="sxs-lookup"><span data-stu-id="17452-118">The **JournalReader** class enables you to load a Journal document stream and to receive an XML stream representing the contents.</span></span> <span data-ttu-id="17452-119">Vous pouvez reconstituer, afficher et manipuler l’encre.</span><span class="sxs-lookup"><span data-stu-id="17452-119">You can reconstitute, display, and manipulate the ink.</span></span>

## <a name="examples"></a><span data-ttu-id="17452-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="17452-120">Examples</span></span>

<span data-ttu-id="17452-121">L’exemple suivant d’un gestionnaire pour l’événement [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) d’un bouton crée une instance de la classe **JournalReader** et l’utilise pour lire un fichier journal existant.</span><span class="sxs-lookup"><span data-stu-id="17452-121">The following example of a handler for a button's [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event creates an instance of the **JournalReader** class and uses it to read an existing Journal file.</span></span>

> [!Note]  
> <span data-ttu-id="17452-122">La méthode **DisplayXml** appelée depuis cet exemple n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="17452-122">The **DisplayXml** method called from this example is not shown.</span></span> <span data-ttu-id="17452-123">L’implémentation spécifique d’une telle méthode dépend des besoins de votre application.</span><span class="sxs-lookup"><span data-stu-id="17452-123">The specific implementation of such a method is dependent on your application's needs.</span></span>

 


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



## <a name="requirements"></a><span data-ttu-id="17452-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17452-124">Requirements</span></span>



| <span data-ttu-id="17452-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17452-125">Requirement</span></span> | <span data-ttu-id="17452-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="17452-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17452-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17452-127">Minimum supported client</span></span><br/> | <span data-ttu-id="17452-128">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17452-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="17452-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17452-129">Minimum supported server</span></span><br/> | <span data-ttu-id="17452-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="17452-130">None supported</span></span><br/>                                                                                         |
| <span data-ttu-id="17452-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="17452-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="17452-132"><dt>Journal. h (nécessite également le journal \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="17452-132"><dt>Journal.h (also requires journal\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="17452-133">DLL</span><span class="sxs-lookup"><span data-stu-id="17452-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17452-134"><dt>Journal.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17452-134"><dt>Journal.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="17452-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17452-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17452-136">GUID de propriété personnalisée</span><span class="sxs-lookup"><span data-stu-id="17452-136">Custom Property GUIDs</span></span>](custom-property-guids.md)
</dt> <dt>

[<span data-ttu-id="17452-137">**Méthode ReadFromStream**</span><span class="sxs-lookup"><span data-stu-id="17452-137">**ReadFromStream Method**</span></span>](ijournalreader-readfromstream.md)
</dt> </dl>

 

