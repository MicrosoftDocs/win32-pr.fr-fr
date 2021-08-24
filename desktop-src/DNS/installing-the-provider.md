---
title: Installation du fournisseur
description: la procédure d’installation du fournisseur WMI DNS diffère selon la version de Windows sur laquelle il est installé.
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- Domain Name System, fournisseur WMI, installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9b4b976ccb1a600f56042cb75b500577335059966a82dbb1f9e77b04f7a4df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693039"
---
# <a name="installing-the-provider"></a>Installation du fournisseur

la procédure d’installation du fournisseur WMI DNS diffère selon la version de Windows sur laquelle il est installé. la procédure suivante décrit comment installer et configurer le fournisseur WMI DNS sur Windows 2000. pour obtenir le fournisseur WMI DNS pour Windows 2000, téléchargez le fichier suivant :

**Avertissement :** Les fichiers de fournisseur WMI DNS ne sont pas interchangeables. les serveurs dns Windows 2000 requièrent des fichiers différents et une procédure différente des serveurs dns Windows Server 2003. La procédure pour chaque est fournie.

**pour installer le fournisseur WMI DNS sur Windows serveur 2000**

1.  procurez-vous le fournisseur WMI DNS pour Windows 2000 à partir du Kit de ressources du serveur Windows 2000 ou téléchargez le fichier, Dnsprov.zip, à partir de : ftp://ftp.microsoft.com/reskit/win2000/
2.  Copiez les fichiers du fournisseur WMI DNS (Dnsprov.dll) et Dnsschema. mof dans le <winntdir> \\ \\ répertoire system32 wbem.
3.  Compilez le fichier MOF. Cela permet de personnaliser le schéma pour qu’il corresponde au serveur.

    **mofcomp Dnsschema. mof**

4.  Inscrivez la DLL sur le serveur DNS.

    **dnsprov.dllregsvr32**

5.  Les scripts ou les programmes qui utilisent le fournisseur WMI DNS pour gérer les serveurs DNS peuvent ensuite être utilisés. Les scripts ou les programmes peuvent être exécutés à partir du serveur DNS ou à partir d’un ordinateur client.
    > [!Note]  
    > Le kit de développement logiciel (SDK) WMI n’est pas requis pour exécuter le fournisseur WMI DNS, mais il contient de nombreux outils utiles.

     

Le fournisseur WMI DNS doit être installé sur n’importe quel serveur DNS à gérer ; Toutefois, les scripts DNS peuvent être exécutés sur le serveur DNS ou sur un hôte distant.

**pour installer le fournisseur WMI DNS sur Windows Server 2003**

-   pour les systèmes d’exploitation Windows Server 2003, le fournisseur WMI DNS est automatiquement installé et inscrit, et son fichier MOF est compilé lors de l’installation du service serveur dns.

 

 




