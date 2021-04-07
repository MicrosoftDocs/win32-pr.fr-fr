---
title: Installation du fournisseur
description: La procédure d’installation du fournisseur WMI DNS diffère selon la version de Windows sur laquelle il est installé.
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- Domain Name System, fournisseur WMI, installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b1c9dbdaf6d3ad55247d0b978c0a422361a2f04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671965"
---
# <a name="installing-the-provider"></a>Installation du fournisseur

La procédure d’installation du fournisseur WMI DNS diffère selon la version de Windows sur laquelle il est installé. La procédure suivante décrit comment installer et configurer le fournisseur WMI DNS sur Windows 2000. Pour obtenir le fournisseur WMI DNS pour Windows 2000, téléchargez le fichier suivant :

**Avertissement :** Les fichiers de fournisseur WMI DNS ne sont pas interchangeables. Les serveurs DNS Windows 2000 requièrent des fichiers différents et une procédure différente des serveurs DNS Windows Server 2003. La procédure pour chaque est fournie.

**Pour installer le fournisseur WMI DNS sur le serveur Windows 2000**

1.  Procurez-vous le fournisseur WMI DNS pour Windows 2000 à partir du kit de ressources du serveur Windows 2000, ou téléchargez le fichier, Dnsprov.zip, à partir de : ftp://ftp.microsoft.com/reskit/win2000/
2.  Copiez les fichiers du fournisseur WMI DNS (Dnsprov.dll) et Dnsschema. mof dans le <winntdir> \\ \\ répertoire system32 wbem.
3.  Compilez le fichier MOF. Cela permet de personnaliser le schéma pour qu’il corresponde au serveur.

    **mofcomp Dnsschema. mof**

4.  Inscrivez la DLL sur le serveur DNS.

    **dnsprov.dllregsvr32**

5.  Les scripts ou les programmes qui utilisent le fournisseur WMI DNS pour gérer les serveurs DNS peuvent ensuite être utilisés. Les scripts ou les programmes peuvent être exécutés à partir du serveur DNS ou à partir d’un ordinateur client.
    > [!Note]  
    > Le kit de développement logiciel (SDK) WMI n’est pas requis pour exécuter le fournisseur WMI DNS, mais il contient de nombreux outils utiles.

     

Le fournisseur WMI DNS doit être installé sur n’importe quel serveur DNS à gérer ; Toutefois, les scripts DNS peuvent être exécutés sur le serveur DNS ou sur un hôte distant.

**Pour installer le fournisseur WMI DNS sur Windows Server 2003**

-   Pour les systèmes d’exploitation Windows Server 2003, le fournisseur WMI DNS est automatiquement installé et inscrit, et son fichier MOF est compilé lors de l’installation du service serveur DNS.

 

 




