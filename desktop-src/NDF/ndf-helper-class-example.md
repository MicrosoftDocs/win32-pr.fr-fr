---
title: Extension de classe d’assistance NDF
description: Cet exemple montre comment implémenter des fonctions de diagnostic et de réparation NDF.
ms.assetid: 18e66d09-e565-4b86-8bc3-600f2159a4bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b2a0dbcba29449b8f21850fa0669f8154dcbd7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507007"
---
# <a name="ndf-helper-class-extension"></a><span data-ttu-id="a4582-103">Extension de classe d’assistance NDF</span><span class="sxs-lookup"><span data-stu-id="a4582-103">NDF Helper Class Extension</span></span>

<span data-ttu-id="a4582-104">Cet exemple montre comment implémenter des fonctions de diagnostic et de réparation NDF.</span><span class="sxs-lookup"><span data-stu-id="a4582-104">This example illustrates how to implement NDF diagnosis and repair functions.</span></span> <span data-ttu-id="a4582-105">Dans cet exemple, un fichier de configuration critique doit exister pour que le système reste sain.</span><span class="sxs-lookup"><span data-stu-id="a4582-105">In this example, a critical configuration file must exist for the system to remain healthy.</span></span> <span data-ttu-id="a4582-106">En conséquence, le problème est de déterminer si le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="a4582-106">Accordingly, the problem is to determine whether the file exists.</span></span> <span data-ttu-id="a4582-107">Si ce n’est pas le cas, le système n’est pas sain et le problème est diagnostiqué par NDF.</span><span class="sxs-lookup"><span data-stu-id="a4582-107">If it does not, the system is unhealthy and the problem is diagnosed by NDF.</span></span> <span data-ttu-id="a4582-108">La réparation consiste à recréer le fichier manquant.</span><span class="sxs-lookup"><span data-stu-id="a4582-108">The repair is to re-create the missing file.</span></span>

<span data-ttu-id="a4582-109">Pour diagnostiquer et résoudre le problème, vous devez utiliser quatre méthodes [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) : [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize), [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth), [**GetRepairInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo)et [**Repair**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair).</span><span class="sxs-lookup"><span data-stu-id="a4582-109">To diagnose and repair the problem requires using four [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) methods: [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize), [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth), [**GetRepairInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo), and [**Repair**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair).</span></span>

## <a name="initializing-the-helper-class"></a><span data-ttu-id="a4582-110">Initialisation de la classe d’assistance</span><span class="sxs-lookup"><span data-stu-id="a4582-110">Initializing the Helper Class</span></span>

<span data-ttu-id="a4582-111">Initialisez et récupérez le nom du fichier à localiser.</span><span class="sxs-lookup"><span data-stu-id="a4582-111">Initialize and retrieve the name of the file to locate.</span></span> <span data-ttu-id="a4582-112">Ce nom de fichier est passé au cours du diagnostic en tant qu’attribut d’assistance appelé « nom de fichier ».</span><span class="sxs-lookup"><span data-stu-id="a4582-112">This filename is passed during diagnosis as a helper attribute called "filename".</span></span>


```C++
#include <windows.h>
//utility function to simplify string allocation and copies, user throughout example
HRESULT 
StringCchCopyWithAlloc (
    PWSTR* Dest, 
    size_t cchMaxLen,
    in PCWSTR Src)
{
    if (NULL == Dest || NULL == Src || cchMaxLen > USHRT_MAX)
    {
        return E_INVALIDARG;
    }
    size_t cchSize = 0;

    HRESULT hr = StringCchLength(Src, cchMaxLen - 1, &cchSize); 
    if (FAILED(hr))
    {
        return hr;
    }

    size_t cbSize = (cchSize + 1)*sizeof(WCHAR);
    *Dest = (PWSTR) CoTaskMemAlloc(cbSize);
    if (NULL == *Dest)
    {
        return E_OUTOFMEMORY;
    }
    SecureZeroMemory(*Dest, cbSize);

    return StringCchCopy((STRSAFE_LPWSTR)*Dest, cchSize + 1, Src);    
}

HRESULT SimpleFileHelperClass::Initialize(
        /* [in] */ ULONG celt,
        /* [size_is][in] */ HELPER_ATTRIBUTE rgAttributes[  ])
{
    if(celt < 1)
    {
        return E_INVALIDARG;
    }
    if(rgAttributes == NULL)
    {
        return E_INVALIDARG; 
    }
    else
    {
        //verify the attribute is named as expected
        if (wcscmp(rgAttributes[0].pwszName, L"filename")==0)
        {
            //copy the attribute to member variable
            return StringCchCopyWithAlloc(&m_pwszTestFile, MAX_PATH, 
                    rgAttributes[0].PWStr);
        } else {
            //the attribute isn't named as expected
            return E_INVALIDARG;
        }
    }
}

```



## <a name="checking-on-the-files-existence"></a><span data-ttu-id="a4582-113">Vérification de l’existence du fichier</span><span class="sxs-lookup"><span data-stu-id="a4582-113">Checking on the File's Existence</span></span>

<span data-ttu-id="a4582-114">La méthode [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) est utilisée pour vérifier l’existence du fichier.</span><span class="sxs-lookup"><span data-stu-id="a4582-114">The [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) method is used to check on the existence of the file.</span></span> <span data-ttu-id="a4582-115">Si le fichier existe, l’état du diagnostic a la valeur **DS \_ rejected**, ce qui indique que rien n’est incorrect.</span><span class="sxs-lookup"><span data-stu-id="a4582-115">If the file exists, diagnosis status is set to **DS\_REJECTED**, indicating nothing is wrong.</span></span> <span data-ttu-id="a4582-116">Si le fichier est introuvable, l’état du diagnostic a la valeur **DS \_ Confirm**.</span><span class="sxs-lookup"><span data-stu-id="a4582-116">If the file cannot be found, the diagnosis status is set to **DS\_CONFIRMED**.</span></span>


```C++
#include <windows.h>

HRESULT SimpleFileHelperClass::LowHealth( 
            /* [unique][string][in] */ LPCWSTR pwszInstanceDescription,
            /* [string][out] */ LPWSTR *ppwszDescription,
            /* [out] */ long *pDeferredTime,
            /* [out] */ DIAGNOSIS_STATUS *pStatus) 

{
    HANDLE hFile = NULL;
    LPWSTR pwszDiagString=NULL;
    // does the file already exist?
    hFile = CreateFile(
        m_pwszTestFile, 
        GENERIC_READ, 
        0, 
        NULL, 
        OPEN_EXISTING, 
        FILE_ATTRIBUTE_NORMAL, 
        NULL);

    if(INVALID_HANDLE_VALUE == hFile)
    { 
        // alloc and set the diagnosis description and status
        HRESULT hr = StringCchCopyWithAlloc(&pwszDiagString, MAX_PATH, 
                    L"The file was deleted.");
        if (FAILED(hr))
        {
            return hr;
        }
  
        *ppwszDescription = pwszDiagString;
        *pStatus = DS_CONFIRMED;
        return S_OK;
    }
    CloseHandle(hFile); 
    
    //the file exists
    *pStatus = DS_REJECTED;
    return S_OK;
}
```



## <a name="determining-the-repair-action"></a><span data-ttu-id="a4582-117">Détermination de l’action de réparation</span><span class="sxs-lookup"><span data-stu-id="a4582-117">Determining the Repair Action</span></span>

<span data-ttu-id="a4582-118">Si [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) retourne **DS \_ Confirm**, [**GetRepairInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo) est implémenté pour déterminer l’action de réparation appropriée.</span><span class="sxs-lookup"><span data-stu-id="a4582-118">If [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) returns **DS\_CONFIRMED**, [**GetRepairInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo) is implemented to determine the appropriate repair action.</span></span> <span data-ttu-id="a4582-119">Dans cet exemple, cela signifie que vous recréez le fichier.</span><span class="sxs-lookup"><span data-stu-id="a4582-119">In this example, that means re-creating the file.</span></span>


```C++
#include <windows.h>

HRESULT  
SimpleFileHelperClass::GetRepairInfo( 
            /* [in] */ PROBLEM_TYPE problem,
            /* [out] */ ULONG *pcelt,
            /* [size_is][size_is][out] */ RepairInfo **ppInfo)
{
    HRESULT hr=S_OK;
    RepairInfo* pRepair = (RepairInfo *)CoTaskMemAlloc(sizeof(RepairInfo));
    if (pRepair == NULL) {
        return E_OUTOFMEMORY;
    }
    SecureZeroMemory(pRepair,sizeof(RepairInfo));

    // set the repair description and class name
    hr = StringCchCopyWithAlloc(&pRepair->pwszClassName, MAX_PATH,
                L"SimpleFileHelperClass");
    if (FAILED(hr))
    {
        goto Error;
    }

    hr = StringCchCopyWithAlloc(&pRepair->pwszDescription, MAX_PATH, 
                L"Low Health Repair");
    if (FAILED(hr))
    {
        goto Error;
    }
  
    // set the resolution GUID and cost
    pRepair->guid = ID_LowHealthRepair;
    pRepair->cost = 0;
    // set repair status flags
    pRepair->sidType = WinWorldSid;
    pRepair->scope = RS_SYSTEM;
    pRepair->risk = RR_NORISK;
    pRepair->flags |= DF_IMPERSONATION; //impersonate the user when repairing
    pRepair->UiInfo.type = UIT_NONE;
    
    //pass back the repair
    *ppInfo = pRepair; 
    *pcelt = 1; //number of repairs

    return S_OK;

Error:
    if(pRepair){
        if(pRepair->pwszClassName){
            CoTaskMemFree(pRepair->pwszClassName);
        }
        if(pRepair->pwszDescription){
            CoTaskMemFree(pRepair->pwszDescription);
        }
    }
    return hr;
}

```



## <a name="repairing-the-problem"></a><span data-ttu-id="a4582-120">Réparation du problème</span><span class="sxs-lookup"><span data-stu-id="a4582-120">Repairing the Problem</span></span>

<span data-ttu-id="a4582-121">L’utilisateur reçoit les options de correction retournées par le [**GetRepairInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo), sauf s’il n’existe qu’une seule option de réparation, auquel cas il est exécuté automatiquement.</span><span class="sxs-lookup"><span data-stu-id="a4582-121">The user is presented with the fix options returned by the [**GetRepairInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo), unless there is only one repair option, in which case it is automatically executed.</span></span> <span data-ttu-id="a4582-122">La méthode de [**réparation**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair) est appelée avec la structure [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) applicable afin que le fichier de configuration puisse être restauré.</span><span class="sxs-lookup"><span data-stu-id="a4582-122">The [**Repair**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair) method is called with the applicable [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) structure so the configuration file can be restored.</span></span>


```C++
#include <windows.h>

HRESULT  
SimpleFileHelperClass::Repair( 
            /* [in] */ RepairInfo *pInfo,
            /* [out] */ long *pDeferredTime,
            /* [out] */ REPAIR_STATUS *pStatus)
{
    //verify expected repair was requested
    if(IsEqualGUID(ID_LowHealthRepair, pInfo->guid)){
        HANDLE hFile = NULL;
        hFile = CreateFile(m_pwszTestFile, 
                                GENERIC_WRITE, 
                                0, 
                                NULL, 
                                CREATE_ALWAYS,
                                FILE_ATTRIBUTE_NORMAL, 
                                NULL);
        if(INVALID_HANDLE_VALUE == hFile)
        {
            // repair failed
            *pStatus = RS_UNREPAIRED;
            return HRESULT_FROM_WIN32(GetLastError());
        }
        CloseHandle(hFile);
        
        // repair succeeded
        *pStatus = RS_REPAIRED;
    } else {
        return E_INVALIDARG; //unkown repair passed in
    }
    return S_OK;
}
```



 

 




