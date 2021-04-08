---
description: Microsoft&\# 160 ; Le fournisseur Win32 récupère et met à jour les données relatives aux systèmes Windows&\# 8212 ; des données telles que les paramètres actuels des variables d’environnement et les attributs d’un disque logique.
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Fournisseur Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dfb29b6f80ed833de0f4185070d46770c6cd2f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747901"
---
# <a name="win32-provider"></a>Fournisseur Win32

Le fournisseur Microsoft Win32 récupère et met à jour les données relatives aux systèmes Windows, telles que les paramètres actuels des variables d’environnement et les attributs d’un disque logique. Avec le fournisseur Win32, les applications de gestion peuvent utiliser WMI pour accéder facilement à ces données. Le fournisseur Win32 récupère ses informations en effectuant des appels de fonction Windows et en interrogeant le registre système.

Le fournisseur Win32 définit les classes utilisées pour décrire le matériel ou les logiciels disponibles sur les systèmes Windows et les relations entre eux.

En tant que fournisseur d’instance et de méthode, le fournisseur Win32 implémente l’interface [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) standard, ainsi que les méthodes [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) suivantes :

-   [**CreateInstanceEnumAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**DeleteInstanceAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [**ExecMethodAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

Le tableau suivant répertorie les catégories de classes du fournisseur Win32.



| Classes                                                                             | Description                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Classes matérielles du système informatique](computer-system-hardware-classes.md)<br/> | Objets liés au matériel.<br/>                                      |
| [Classes du système d’exploitation](operating-system-classes.md)<br/>                 | Objets associés au système d’exploitation.<br/>                              |
| [Classes du compteur de performances](performance-counter-classes.md)<br/>           | Données de performances brutes et calculées à partir des compteurs de performances.<br/> |
| [Classes de gestion des services WMI](wmi-service-management-classes.md)<br/>     | Gestion pour WMI.<br/>                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fournisseur WMI CIMWin32](cimwin32-wmi-providers.md)
</dt> </dl>

 

 
