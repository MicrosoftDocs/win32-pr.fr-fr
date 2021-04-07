---
title: Activation des modifications de schéma au niveau du contrôleur de schéma
description: Par défaut, la modification du schéma est désactivée sur tous les contrôleurs de domaine Windows 2000.
ms.assetid: 08806a9e-283c-48d9-9557-bcb9719fc13c
ms.tgt_platform: multiple
keywords:
- Activation des modifications de schéma au niveau de l’AD du contrôleur de schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4840c9928011179ce303c83f4d00ef598f38eb64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939643"
---
# <a name="enabling-schema-changes-at-the-schema-master"></a><span data-ttu-id="758f6-104">Activation des modifications de schéma au niveau du contrôleur de schéma</span><span class="sxs-lookup"><span data-stu-id="758f6-104">Enabling Schema Changes at the Schema Master</span></span>

<span data-ttu-id="758f6-105">Par défaut, la modification du schéma est désactivée sur tous les contrôleurs de domaine Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="758f6-105">By default, schema modification is disabled on all Windows 2000 domain controllers.</span></span> <span data-ttu-id="758f6-106">La possibilité de mettre à jour le schéma est contrôlée par la valeur de Registre suivante sur le contrôleur de domaine principal du schéma :</span><span class="sxs-lookup"><span data-stu-id="758f6-106">The ability to update the schema is controlled by the following registry value on the schema master domain controller:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            NTDS
               Parameters
                  Schema Update Allowed
```

<span data-ttu-id="758f6-107">Cette valeur de Registre est une valeur **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="758f6-107">This registry value is a **REG\_DWORD** value.</span></span> <span data-ttu-id="758f6-108">Si cette valeur est absente ou si elle contient zéro (0), la modification du schéma est désactivée.</span><span class="sxs-lookup"><span data-stu-id="758f6-108">If this value is not present or contains zero (0), then schema modification is disabled.</span></span> <span data-ttu-id="758f6-109">Si cette valeur est présente et contient une valeur différente de zéro, la modification de schéma est activée.</span><span class="sxs-lookup"><span data-stu-id="758f6-109">If this value is present and contains a value other than zero, then schema modification is enabled.</span></span>

<span data-ttu-id="758f6-110">Le composant logiciel enfichable MMC du gestionnaire de schémas offre à l’utilisateur la possibilité d’activer ou de désactiver manuellement la modification du schéma.</span><span class="sxs-lookup"><span data-stu-id="758f6-110">The Schema Manager MMC snap-in provides the user with the ability to manually enable or disable schema modification.</span></span> <span data-ttu-id="758f6-111">La modification de schéma peut être activée ou désactivée par programme en modifiant cette valeur de Registre sur le contrôleur de domaine principal du schéma.</span><span class="sxs-lookup"><span data-stu-id="758f6-111">Schema modification can be enabled or disabled programmatically by modifying this registry value on the schema master domain controller.</span></span>

<span data-ttu-id="758f6-112">La fonction C++ suivante montre comment déterminer si le schéma peut être modifié sur un contrôleur de schéma spécifié.</span><span class="sxs-lookup"><span data-stu-id="758f6-112">The following C++ function shows how to determine if the schema can be modified on a specified schema master.</span></span>


```C++
HRESULT IsSchemaUpdateEnabled(
    LPTSTR pszSchemaMasterComputerName, 
    BOOL *pfEnabled)
{
    *pfEnabled = FALSE;
  
    LPTSTR szPrefix = "\\\\";
    LPTSTR pszPath = new TCHAR[lstrlen(szPrefix) + 
        lstrlen(pszSchemaMasterComputerName) + 1];
    if(!pszPath)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = E_FAIL;
    LONG lReturn;
    HKEY hKeyMachine;

    tcscpy_s(pszPath, szPrefix);
    tcscat_s(pszPath, pszSchemaMasterComputerName);
    lReturn = RegConnectRegistry(
        pszPath, 
        HKEY_LOCAL_MACHINE, 
        &hKeyMachine);
    
    delete [] pszPath;

    if (ERROR_SUCCESS == lReturn)
    {
        HKEY hKeyParameters;
        LPTSTR szKeyPath = 
          TEXT("System\\CurrentControlSet\\Services\\NTDS\\Parameters");
        LPTSTR szValueName = TEXT("Schema Update Allowed");

        lReturn = RegOpenKeyEx(
            hKeyMachine, 
            szKeyPath, 
            0, 
            KEY_READ, 
            &hKeyParameters);
        if (ERROR_SUCCESS == lReturn)
        {
            DWORD dwType;
            DWORD dwValue;
            DWORD dwSize;

            dwSize = sizeof(dwValue);
            lReturn = RegQueryValueEx(
                hKeyParameters, 
                szValueName, 
                0, 
                &dwType, 
                (LPBYTE)&dwValue, 
                &dwSize);
            if (ERROR_SUCCESS == lReturn)
            {
                *pfEnabled = (0 != dwValue);
                
                hr = S_OK;
            }
            
            RegCloseKey(hKeyParameters);
        }
    
        RegCloseKey(hKeyMachine);
    }
  
    return hr;
}
```



<span data-ttu-id="758f6-113">La fonction C++ suivante montre comment activer ou désactiver la modification de schéma sur un contrôleur de schéma spécifié.</span><span class="sxs-lookup"><span data-stu-id="758f6-113">The following C++ function shows how to enable or disable schema modification on a specified schema master.</span></span>


```C++
HRESULT EnableSchemaUpdate(
    LPTSTR pszSchemaMasterComputerName, 
    BOOL fEnabled)
{
    
    LPTSTR szPrefix = "\\\\";
    LPTSTR pszPath = new TCHAR[lstrlen(szPrefix) + 
        lstrlen(pszSchemaMasterComputerName) + 1];
    if(!pszPath)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = E_FAIL;
    LONG lReturn;
    HKEY hKeyMachine;

    strcpy_s(pszPath, szPrefix);
    strcat_s(pszPath, pszSchemaMasterComputerName);
    lReturn = RegConnectRegistry(
        pszPath, 
        HKEY_LOCAL_MACHINE, 
        &hKeyMachine);
    
    delete [] pszPath;

    if (ERROR_SUCCESS == lReturn)
    {
        HKEY hKeyParameters;
        LPTSTR szRelKeyPath = 
          TEXT("System\\CurrentControlSet\\Services\\NTDS\\Parameters");
        LPTSTR szValueName = TEXT("Schema Update Allowed");

        lReturn = RegOpenKeyEx(
            hKeyMachine, 
            szRelKeyPath, 
            0, 
            KEY_SET_VALUE, 
            &hKeyParameters);
        if (ERROR_SUCCESS == lReturn)
        {
            DWORD dwValue;
            DWORD dwSize;

            if(fEnabled)
            {
                dwValue = 1;
            }
            else
            {
                dwValue = 0;
            }
            
            dwSize = sizeof(dwValue);
            lReturn = RegSetValueEx(
                hKeyParameters, 
                szValueName, 
                0L, 
                REG_DWORD, 
                (LPBYTE)&dwValue, 
                dwSize);
            if (ERROR_SUCCESS == lReturn)
            {
                hr = S_OK;
            }
            
            RegCloseKey(hKeyParameters);
        }
    
        RegCloseKey(hKeyMachine);
    }
    
    return hr;
}
```



 

 




