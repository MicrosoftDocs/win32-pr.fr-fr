---
title: Inscription des extensions de classe d’assistance NDF
description: Chaque extension de classe d’assistance est associée à un certain nombre de clés de registre. Certaines clés sont requises par COM, et certaines clés sont requises par NDF.
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6457e144abdeb1dbed1e33bb10e21302f918da8cdc5a6fd2090f3665e83f0316
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798496"
---
# <a name="registering-ndf-helper-class-extensions"></a>Inscription des extensions de classe d’assistance NDF

Chaque extension de classe d’assistance est associée à un certain nombre de clés de registre. Certaines clés sont requises par COM, et certaines clés sont requises par NDF.

## <a name="com-registry-keys"></a>Clés de registre COM

Les extensions de classe d’assistance doivent être implémentées en tant que serveurs COM. L’inscription COM doit être effectuée pour chaque extension de la classe d’assistance. Le CLSID de l’objet, l’interface [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) et l’interface [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) doivent être inscrits. L’inscription crée un certain nombre de clés de Registre liées à COM pour l’extension de classe d’assistance NDF.

## <a name="ndf-registry-keys"></a>Clés de Registre NDF

Les extensions de classe d’assistance doivent être inscrites avant l’interaction avec l’infrastructure de diagnostics réseau et avec d’autres classes d’assistance associées. Pour ce faire, vous devez remplir le registre.

La procédure suivante montre comment ajouter des extensions de classe d’assistance au registre.

1.  Publiez les noms des classes d’assistance implémentées par la DLL et leurs dépendances en créant une clé pour la DLL sous

    **HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *NomFournisseur* \\ **HostDLLs** \\ *classe d’assistance dll* \\ **HelperClasses** \\ *nom de classe d’assistance*

    Remplacez *NomFournisseur*, *dll de la classe d’assistance* et le nom de la *classe d’assistance* par des valeurs définies par l’utilisateur, comme décrit ci-dessous.

    | Valeur               | Type    | Signification                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | *VendorName*        | SZ de REG \_ | Nom du fournisseur.                                                      |
    | *DLL de la classe d’assistance*  | SZ de REG \_ | Nom de la DLL, sans extension.                                          |
    | *Nom de la classe d’assistance* | SZ de REG \_ | Nom de la classe d’assistance dont dépend la classe d’assistance actuelle. |

    

     

2.  Sous chaque clé de *nom de classe d’assistance* , publiez les informations suivantes.

    

    | Valeur         | Type       | Signification                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **IDENTIFICATEUR**     | SZ de REG \_    | Chaîne qui contient l’ID de classe COM de la classe d’assistance.                                                                                                            |
    | **Version**   | SZ de REG \_    | Chaîne qui contient les versions principales et secondaires de la classe d’assistance dans le format <major> <minor> .                                                        |
    | **Publié** | \_valeur DWORD reg | La valeur 1 signifie que cette classe d’assistance est supposée être appelée directement à partir du client de diagnostic. 0 signifie qu’il ne peut être appelé qu’à partir d’une autre classe d’assistance. |
    | **Parent**    | SZ de REG \_    | Chaîne qui nomme la classe d’assistance extensible Microsoft qui est étendue.                                                                                       |

    

     

3.  Pour chaque classe d’assistance, publiez la liste des attributs correspondants en créant une clé sous

    **HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *NomFournisseur* \\ **HostDLLs** \\ *classe d’assistance dll* \\ **HelperClasses** \\ *nom de classe d’assistance* \\ **MatchAttributes**

    Elles doivent contenir une ou plusieurs valeurs (une par attribut) du type suivant.

    | Valeur             | Type                             | Signification                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | **AttributeName** | reg \_ SZ \| reg \_ \| \_ fichier binaire reg | Valeur qui complète la paire nom/valeur d’un attribut particulier. |

    

     

 

 




