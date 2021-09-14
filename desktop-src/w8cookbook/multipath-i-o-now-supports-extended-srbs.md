---
title: MPIO (Multipath I/O) prend désormais en charge les blocs de demande de stockage étendu
description: MPIO (Multipath I/O) prend désormais en charge les blocs de demande de stockage étendu
ms.assetid: 5373D9ED-34AF-4D66-8888-49F1EBF768F4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f558f8088b5066b51447c5f2ea23edd5154d5c10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196196"
---
# <a name="multipath-io-now-supports-extended-storage-request-blocks"></a>MPIO (Multipath I/O) prend désormais en charge les blocs de demande de stockage étendu

## <a name="platforms"></a>Plateformes

**serveurs** – Windows Server 2012 

## <a name="description"></a>Description

dans Windows Server 2012, une nouvelle structure, le bloc de demande de stockage \_ \_ (srb étendu) remplace \_ le \_ bloc de requête SCSI (srb hérité) dans la pile de stockage de base. Les SRBs étendus répliquent les fonctionnalités des SRBs hérités, mais sont également extensibles et évolutives.

MPIO (Multipath I/O) prend en charge les SRBs étendus et permet aux modules DSM (Device Specific modules) de spécifier également la prise en charge de SRB étendue. Toutefois, pour que la pile de stockage d’un appareil à chemins d’accès multiples utilise des SRBs étendus, **tous les composants de la pile doivent prendre en charge les SRBs étendus, y compris le module DSM**. Notez que le module de la compatibilité des boîtiers Microsoft, MSDSM, prend en charge les SRBs étendus.

La \_ structure SCSI pass-through ne \_ \_ fait pas partie de la structure de transfert MPIO étendu, car la transmission SCSI étendue peut être de taille variable, en fonction du débogueur de ligne de commande (CDB). Au lieu de cela, le transfert MPIO étendu a un champ qui décrit le décalage entre le début de la structure de transfert MPIO étendu et \_ la \_ structure pass-through SCSI \_ . L’appelant doit s’assurer qu’il alloue une mémoire tampon de la taille appropriée et définir correctement le décalage de passage SCSI. Tant que l’appelant respecte les règles pour les passes SCSI étendues, il ne doit pas y avoir de travail supplémentaire pour utiliser le transfert MPIO étendu.

> [!Note]  
> Si le module DSM ne prend pas en charge les SRBs étendus, MPIO échouera avec les demandes de transfert MPIO étendu qui ont l’indicateur \_ \_ \_ DSM IOCTL \_ défini.

 

## <a name="manifestation"></a>Manifestation

Si une partie de la pile de stockage de l’appareil, y compris le DSM, ne prend pas en charge les SRBs étendus, la pile de stockage est restaurée en utilisant des SRBs hérités.

## <a name="solution"></a>Solution

Il n’existe que deux exigences MPIO pour qu’un module DSM prenne en charge les blocs de demande de stockage \_ \_ :

-   Le DSM doit signaler son type en tant que DsmType6
-   Le module DSM doit fournir la \_ \_ \_ fonction prise en charge du type d’adresse DSM

Si le DSM ne signale pas DsmType6 ou s’il signale DsmType6 mais ne fournit pas la \_ fonction de type d’adresse DSM \_ \_ prise en charge, MPIO suppose que le module DSM ne prend pas en charge les SRBs étendus.

La \_ \_ fonction de type d’adresse DSM \_ pris en charge accepte deux paramètres, dont l’un est un type d’adresse. Ce type d’adresse doit être l’une des \_ valeurs de type d’adresse de stockage \_ \_ \* définies dans SRB. h. Le module DSM doit retourner la valeur TRUE s’il prend en charge le type d’adresse donné et FALSe dans le cas contraire. La définition de « support » correspond finalement au DSM. MPIO utilise cette fonction pour s’assurer que le module DSM ne se comportera pas de façon incorrecte s’il reçoit un SRB étendu avec une \_ structure d’adresse Stor du type donné. Par conséquent, MPIO appelle généralement cette fonction lorsqu’un périphérique à chemins d’accès multiples est énuméré, mais que la fonction peut être appelée à tout moment.

Si un DSM ne touche pas l’adresse STOR d’un service SRB étendu \_ , il peut retourner la valeur true pour toute valeur de type d’adresse de stockage valide \_ \_ \_ \* . Examinez l’exemple de DSM dans le kit WDK.

**Autres remarques importantes**

-   Les DSM qui prennent en charge les SRBs étendus doivent pouvoir gérer à la fois les structures \_ \_ de bloc de requête SCSI et les structures de bloc de demande de stockage \_ \_ . La seule raison pour laquelle un DSM signale qu’il prend en charge le SRBs étendu ne signifie pas qu’il recevra exclusivement des SRBs étendus. Il peut toujours recevoir un nombre quelconque de SRBs hérités en plus des SRBs étendus, et doit donc être en mesure de gérer les deux.
-   Nous avons fourni un fichier d’en-tête dans le kit WDK appelé srbhelper. h, qui contient des fonctions inline pour aider les pilotes qui doivent gérer à la fois les SRBs étendus et les hérités. Notre exemple de DSM utilise cet en-tête, ce qui vous permet de l’utiliser comme exemple d’utilisation de ces fonctions.
-   Un module DSM qui ne prend pas en charge les SRBs étendus ne doit jamais gérer les SRBs étendus.
-   Il est possible qu’une MPIO fasse basculer la pile de stockage sur les SRBs hérités dans le cas où le DSM ne prend pas en charge un type d’adresse de stockage donné \_ \_ \_ \* (mais prend en charge les SRBs étendus).
-   « BTL8 » est le seul \_ \_ type d’adresse \_ \* de stockage actuellement défini pour Windows Server 2012.

 

 




