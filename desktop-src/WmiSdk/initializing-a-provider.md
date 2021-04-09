---
description: L’une des premières tâches à coder pour un fournisseur est le processus d’initialisation, qui couvre toutes les tâches que votre fournisseur doit effectuer, qui lui permet d’envoyer et de recevoir des informations à partir de WMI, de contrôler un objet géré et d’effectuer d’autres tâches.
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: Initialisation d’un fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14a724d72d5e5c58eff30f2fa61da64d77a493f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868750"
---
# <a name="initializing-a-provider"></a>Initialisation d’un fournisseur

L’une des premières tâches à coder pour un fournisseur est le processus d’initialisation, qui couvre toutes les tâches que votre fournisseur doit effectuer, qui lui permet d’envoyer et de recevoir des informations à partir de WMI, de contrôler un objet géré et d’effectuer d’autres tâches. Chaque type de fournisseur a un ensemble différent de tâches qu’il doit effectuer et un ensemble d’interfaces uniques.

Toutefois, tous les fournisseurs s’initialisent par le biais de l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) et informent WMI de leur état d’initialisation par le biais de l’interface [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) .

La procédure suivante décrit comment initialiser un fournisseur.

**Pour initialiser un fournisseur**

1.  Implémentez [**IWbemProviderInit :: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) pour votre fournisseur.

    Lorsque WMI détermine qu’un client requiert les services d’un fournisseur, WMI charge le fournisseur en appelant la méthode [**IWbemProviderInit :: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) .

2.  Implémentez toutes les interfaces propres à votre type de fournisseur.
3.  Informez WMI que votre fournisseur a fini d’être initialisé en appelant [**IWbemProviderInitSink :: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).

    Toutes les implémentations de [**IWbemProviderInit :: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) doivent appeler [**IWbemProviderInitSink :: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) pour signaler l’état d’initialisation à WMI. La méthode **SetStatus** permet à WMI de déterminer si un fournisseur est prêt à recevoir des demandes et le type de demandes que le fournisseur est prêt à recevoir.

La procédure suivante décrit comment signaler une initialisation réussie.

**Pour signaler une initialisation réussie**

-   Définissez le paramètre *IStatus* de [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) sur **WBEM \_ . \_**

    En retournant **WBEM \_ S \_ initialisé**, un fournisseur indique une préparation pour gérer les demandes des applications, WMI et d’autres fournisseurs. Après la réception de WBEM \_ \_ , WMI effectue un appel à la méthode [**IWbemProviderInit :: QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) sur le fournisseur. Cette requête récupère un pointeur vers l’interface principale du fournisseur.

La procédure suivante décrit comment signaler une erreur pendant l’initialisation.

**Pour signaler une erreur pendant l’initialisation**

-   **\_ \_ Échec** de la définition du paramètre *IStatus* de [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) à WBEM. Les fournisseurs d’affichages WMI qui renvoient **WBEM \_ E \_ échouent** comme non fonctionnels.

    WMI libère le pointeur [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) une fois que WMI a obtenu un pointeur vers l’interface principale du fournisseur ou après l’échec de l’initialisation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’un fournisseur WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sécurisation de votre fournisseur](securing-your-provider.md)
</dt> </dl>

 

 



