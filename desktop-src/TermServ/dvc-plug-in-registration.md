---
title: Inscription du plug-in DVC
description: Décrit la syntaxe de l’entrée de plug-in de canal virtuel dynamique (DVC) pour le client Connexion Bureau à distance (RDC).
ms.assetid: cda4f8c9-867a-41ac-894a-4296d5912b2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 183c73f5f9dda0321640119b2750776d207973cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511314"
---
# <a name="dvc-plug-in-registration"></a>Inscription du plug-in DVC

Le plug-in de canal virtuel dynamique (DVC) est inscrit pour une utilisation par le client Connexion Bureau à distance (RDC) à l’aide de l’une des méthodes suivantes :

-   Appel de la méthode [**IMsTscAdvancedSettings ::p ut \_ PluginDlls**](imstscadvancedsettings-plugindlls.md) du contrôle ActiveX protocole RDP (Remote Desktop Protocol) (RDP). Les entrées multiples doivent être séparées par des virgules.
-   Écriture de l’entrée de plug-in à l’emplacement suivant dans le registre sur l’ordinateur où est démarré le processus client Connexion Bureau à distance (RDC) :

    **HKEY \_ \_** \\  \\  \\  \\  \\  \\ ***Nom du plug-*** in par défaut des compléments Microsoft Terminal Server client du logiciel utilisateur actuel

    > [!Note]  
    > Vous devez créer la sous-clé *de nom de plug-in unique* si elle n’existe pas. Le nom de la sous-clé du *nom de plug-in unique* est une chaîne arbitraire qui peut identifier le plug-in. La chaîne peut être n’importe quelle combinaison de caractères.

     

    Sous *nom de plug-in unique*, vous devez ajouter une entrée qui identifie le plug-in.

    Nom de l’entrée = **nom**

    Type de données = **reg \_ SZ** ou **reg \_ expand \_ SZ**

Dans les deux cas, la valeur d’entrée doit être conforme à l’un des formats suivants :

<dl> <dt>

<span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>«*Plug-inDLLName*: {*CLSID*} »
</dt> <dd>

Le plug-in n’est pas nécessairement inscrit dans le Registre Windows en tant qu’objet COM (Component Object Model), mais la DLL est implémentée en tant qu’objet COM in-process. Le client RDC charge la DLL spécifiée par *Plug-inDLLName* et récupère l’objet com directement à l’aide du *CLSID*.

</dd> <dt>

<span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>«*Plug-inDLLName*»
</dt> <dd>

La DLL implémente la fonction [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) et l’exporte par nom. Le client RDC utilise la fonction **VirtualChannelGetInstance** pour obtenir les pointeurs d’interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) pour tous les plug-ins implémentés par la dll.

</dd> <dt>

<span id="_CLSID_"></span><span id="_clsid_"></span>« {*CLSID*} »
</dt> <dd>

Le client RDC instancie le plug-in en tant qu’objet COM normal à l’aide de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) avec le *CLSID*.

</dd> </dl>

> [!Note]  
> *Plug-inDLLName* représente le chemin d’accès complet et le nom du fichier. dll. Si le type de données est **reg \_ expand \_ SZ**, le chemin d’accès peut contenir des variables d’environnement non développées qui sont développées au moment de l’exécution.

 

Lorsque le client Connexion Bureau à distance (RDC) termine son initialisation, il effectue les opérations suivantes pour chaque plug-in inscrit :

1.  Obtenez une instance de l’interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) pour chaque plug-in à l’aide de l’une des méthodes décrites ci-dessus.
2.  Appelez la méthode [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) de chaque interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) .
3.  Si le client se connecte plusieurs fois au même serveur ou à un autre serveur, il peut y avoir plusieurs appels aux méthodes [**connectées**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) et [**déconnectées**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) .
4.  Le dernier appel que le plug-in doit gérer est [**terminé**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated). Le client Connexion Bureau à distance (RDC) est sur le point de décharger le plug-in.

 

 