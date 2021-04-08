---
title: Modification du registre de Windows 95
description: Vous pouvez utiliser REGEDIT pour modifier le Registre Windows 95 afin de désigner un NSP.
ms.assetid: 109daf4a-722f-4a25-a778-72360ee07ad9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c622ea44a5e365ca631d6d4db34af8e939ea6487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840657"
---
# <a name="editing-the-windows-95-registry"></a>Modification du registre de Windows 95

Vous pouvez utiliser REGEDIT pour modifier le Registre Windows 95 afin de désigner un NSP.

**Pour désigner un fournisseur de services de noms Microsoft Locator pour Windows 95**

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

    

     

Vous pouvez utiliser REGEDIT pour modifier le Registre Windows 95 afin de désigner un NSP CDS CDS.

**Pour désigner un fournisseur de services de noms de CD DCE pour Windows 95**

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

     

 

 





