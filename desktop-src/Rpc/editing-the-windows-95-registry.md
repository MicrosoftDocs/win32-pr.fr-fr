---
title: modification du registre Windows 95
description: vous pouvez utiliser REGEDIT pour modifier le registre Windows 95 afin de désigner un NSP.
ms.assetid: 109daf4a-722f-4a25-a778-72360ee07ad9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4442ef9984110fb0d912e4e5e90e00b7d14222bc16044c02f9570fe3e714c066
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021649"
---
# <a name="editing-the-windows-95-registry"></a>modification du registre Windows 95

vous pouvez utiliser REGEDIT pour modifier le registre Windows 95 afin de désigner un NSP.

**pour désigner un fournisseur de services de noms Microsoft Locator pour Windows 95**

1.  Sélectionnez

    **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **RPC**

2.  Créer une nouvelle clé appelée

    **NameService**

3.  Une fois la clé **NameService** sélectionnée, créez les noms de **StringValue** et modifiez-les pour qu’ils contiennent les données, comme indiqué dans le tableau suivant.

    

    | Nom                     | Données                                                                        |
    |--------------------------|-----------------------------------------------------------------------------|
    | **DefaultSyntax**        | 3<br/>                                                                |
    | **Protocole**             | ncacn \_ NP<br/>                                                        |
    | **Point de terminaison**             | \\Localisateur de canal \\<br/>                                                  |
    | **NetworkAddress**       | MyServer (où MyServer est le nom de l’ordinateur Windows NT)<br/> |
    | **ServerNetworkAddress** | MyServer<br/>                                                         |

    

     

vous pouvez utiliser REGEDIT pour modifier le registre Windows 95 afin de désigner un NSP CDS CDS.

**pour désigner un fournisseur de services de noms de cd DCE pour Windows 95**

1.  Sélectionnez

    **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **RPC**

2.  Créer une nouvelle clé appelée

    **NameService**

3.  Une fois la clé **NameService** sélectionnée, créez les noms de **StringValue** et modifiez-les pour qu’ils contiennent les données, comme indiqué dans le tableau suivant.

    

    | Nom                     | Données                                                             |
    |--------------------------|------------------------------------------------------------------|
    | **DefaultSyntax**        | 3<br/>                                                     |
    | **Protocole**             | \_TCP IP \_ ncacn<br/>                                        |
    | **Point de terminaison**             | "" (chaîne vide)<br/>                                  |
    | **NetworkAddress**       | monserveur (nom de l’ordinateur hôte exécutant NSID)<br/> |
    | **ServerNetworkAddress** | monserveur (nom de l’ordinateur hôte exécutant NSID)<br/> |

    

     

    > [!Note]  
    > Vous devez avoir le produit DCE service d’annuaire de cellules/service d’annuaires de cellules Digital Equipment Corporation pour configurer les CDS DCE en tant que fournisseur de services de noms. Consultez la documentation fournie par Digital Equipment Corporation pour plus d’informations sur les CDS DCE.

     

 

 





