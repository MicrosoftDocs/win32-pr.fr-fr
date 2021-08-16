---
description: Avant d’appeler l’une des fonctions de base de données suivantes à partir d’un programme, par exemple une action personnalisée ou un processus Automation, le programme d’installation doit d’abord exécuter l’action CostInitialize, l’action FileCost et l’action CostFinalize.
ms.assetid: b9795825-41fa-474b-a0c5-06770aa99bc1
title: Appel de fonctions de base de données à partir de programmes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1959e43b680d84e04de1f68483e8a1016bbeca0e867daebf10a317838d68c0ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145702"
---
# <a name="calling-database-functions-from-programs"></a>Appel de fonctions de base de données à partir de programmes

Avant d’appeler l’une des [fonctions de base de données](database-functions.md) suivantes à partir d’un programme, par exemple une action personnalisée ou un processus Automation, le programme d’installation doit d’abord exécuter l’action [CostInitialize](costinitialize-action.md), l’action [FileCost](filecost-action.md)et l' [action CostFinalize](costfinalize-action.md).

la liste suivante répertorie les fonctions de base de données utilisées dans Windows Installer :

-   [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
-   [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)
-   [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
-   [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)
-   [**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)
-   [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)
-   [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)
-   [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)
-   [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)
-   [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha)
-   [**MsiVerifyDiskSpace**](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)

Avant d’appeler [**MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa) à partir d’un programme, le programme d’installation doit d’abord exécuter l’action CostInitialize. Le programme d’installation exécute ensuite l’action CostFinalize après **MsiSetFeatureAttributes**.

L’exemple suivant illustre l’ordre dans lequel les actions de fonction doivent être appelées lors de l’utilisation de [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) dans un programme.


```C++
#include <windows.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib") 

int main()  
{ 

MSIHANDLE hInstall;
TCHAR *szBuf;
DWORD cch  = 0 ;
 
if(MsiOpenPackage(_T("PathToPackage...."), &hInstall) == ERROR_SUCCESS)
{
    if(MsiDoAction(hInstall, _T("CostInitialize"))==ERROR_SUCCESS  
        && MsiDoAction(hInstall, _T("FileCost"))==ERROR_SUCCESS  
        && MsiDoAction(hInstall, _T("CostFinalize"))==ERROR_SUCCESS)   
    { 
        if(MsiGetTargetPath(hInstall, _T("FolderName"), _T(""),&cch)==ERROR_MORE_DATA)
        { 
            cch++; // add 1 to include null terminator since MsiGetTargetPath does not include it on return 
            szBuf = (TCHAR *) malloc(cch*sizeof(TCHAR));
            if(szBuf)
            {
                if(MsiGetTargetPath(hInstall, _T("FolderName"), szBuf,&cch)==ERROR_SUCCESS)
                {
                    // Add code to use szBuf here
                }
                free(szBuf);
            }
        } 
    } 
    MsiCloseHandle(hInstall);
}

return 0;  
}
```



 

 



