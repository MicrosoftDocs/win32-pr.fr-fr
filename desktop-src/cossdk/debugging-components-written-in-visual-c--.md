---
description: Lorsque vous êtes prêt à déboguer la fonctionnalité COM+ dans vos composants Microsoft Visual C++, vous pouvez configurer Visual C++ projet ou l’outil d’administration Services de composants pour lancer le débogueur.
ms.assetid: 206467ac-108a-49de-a884-66959dc77650
title: Débogage de composants écrits en Visual C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e4b6324cc69531f09612c2af37fa03a036fd4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516770"
---
# <a name="debugging-components-written-in-visual-c"></a>Débogage de composants écrits en Visual C++

Lorsque vous êtes prêt à déboguer la fonctionnalité COM+ dans vos composants Microsoft Visual C++, vous pouvez configurer Visual C++ projet ou l’outil d’administration Services de composants pour lancer le débogueur. Si vous utilisez Visual C++, vous pouvez déboguer avec un client distant en utilisant OLE RPC et le débogage juste-à-temps (JIT). Si vous ne parvenez pas à exécuter votre client sous le débogueur ou si le client s’exécute sur un autre ordinateur, vous pouvez utiliser le paramètre **de lancement de com+ dans le débogueur** . Vous le trouverez dans l’outil d’administration Services de composants comme une case à cocher sous l’onglet **avancé** de la boîte de dialogue **Propriétés** de l’application com+.

Lorsque vous avez terminé le débogage, vous devez arrêter les applications COM+ que vous déboguez. Si un processus serveur est en cours d’exécution, vous pouvez recevoir un message d’erreur la prochaine fois que vous essaierez de générer une DLL lorsque la DLL existante sera encore chargée en mémoire. Pour arrêter une application COM+, cliquez avec le bouton droit sur l’application dans l’arborescence de la console, puis cliquez sur **arrêter**.

> [!Note]  
> Si vous utilisez des transactions, vous pouvez également augmenter le délai d’expiration de la transaction, qui est par défaut de 60 secondes. Vous pouvez également spécifier la valeur 0, en spécifiant un délai d’expiration de transaction infini. À l’aide de l’outil d’administration Services de composants, modifiez le paramètre de délai d’expiration de la transaction sous l’onglet **options** de la fenêtre **Propriétés du poste de travail** .

 

## <a name="debugging-server-application-components-with-visual-c"></a>Débogage des composants d’application serveur avec Visual C++

Lors du débogage d’applications serveur COM+, vous pouvez déboguer des appels distants en chargeant le client et l’application serveur dans le débogueur. Avec Visual C++, vous pouvez déboguer des appels distants à vos composants via les paramètres JIT (Just-in-Time) et OLE RPC. Le paramètre JIT fait en sorte que le composant compilé démarre le débogueur Visual C++ lorsqu’une erreur se produit ; le paramètre OLE RPC permet au débogueur d’effectuer un pas à pas du client au composant à mesure que vous parcourez votre code.

Lorsque ces fonctionnalités sont activées, vous pouvez démarrer votre client sous le débogueur. Lorsque le client effectue un appel à votre composant, le débogueur effectue un pas à pas détaillé dans le code du composant dans le processus serveur, même si le serveur se trouve sur un autre ordinateur sur le réseau. Une session de débogage est automatiquement démarrée sur l’ordinateur serveur, si nécessaire. De même, l’exécution pas à pas unique de l’instruction return dans le code du composant retourne le débogage à l’instruction suivante dans le code du client.

> [!Note]  
> Vous pourrez peut-être enregistrer quelques étapes à l’aide du paramètre **de lancement de com+ dans le débogueur** . Cela vous permet de spécifier le débogueur Visual C++ (ou autre) sans avoir à définir des paramètres de débogage spéciaux dans l’environnement Visual C++. Vous le trouverez dans l’outil d’administration Services de composants comme une case à cocher sous l’onglet **avancé** de la boîte de dialogue **Propriétés** de l’application com+. Pour plus d’informations, consultez « Débogage sans Visual C++ » dans cette rubrique.

 

Lorsque l’application COM+ contenant votre composant est une application serveur, vous devez commencer par arrêter l’application à l’aide de l’outil d’administration Services de composants. Pour ce faire, cliquez avec le bouton droit sur l’application COM+ dans l’arborescence de la console, puis cliquez sur **arrêter**.

**Pour activer le débogage RPC dans Visual C++**

1.  Dans Visual C++, dans le menu **Outils** , cliquez sur **options**.

2.  Dans la boîte de dialogue **options** , sous l’onglet **Déboguer** , activez les cases à cocher débogage **OLE RPC** et **débogage juste-à-temps** .

3.  Cliquez sur **OK**.

Pour commencer le débogage, démarrez votre projet client dans le débogueur.

Vous pouvez également déboguer votre composant sans lancer votre client dans le débogueur. Dans ce cas, votre composant doit lancer le débogueur seul. Pour ce faire, votre projet de composant doit spécifier un fichier exécutable pour la session de débogage, ainsi que l’ID de l’application COM+.

**Pour permettre à un composant d’application serveur de lancer le débogueur Visual C++**

1.  Dans le menu **projet** , cliquez sur **paramètres**.

2.  Dans la boîte de dialogue **paramètres du projet** , dans la zone **paramètres pour** , sélectionnez **débogage Win32**.

3.  Sous l’onglet **Déboguer** , dans la zone **catégorie** , sélectionnez **général**.

4.  Dans la zone **exécutable pour la session de débogage** , entrez le chemin d’accès complet de Dllhost.exe, suivi d’un argument spécifiant l’ID d’application de l’application com+ contenant le composant.

    > [!Note]  
    > À l’aide de l’outil d’administration Services de composants, vous trouverez l’ID de l’application sous l’onglet **général** de la boîte de dialogue **Propriétés** de l’application com+. Vous trouverez ci-dessous un exemple :

     

    > [!Note]  
    > C : \\ winnt winnt \\ \\Dllhost.exe/ProcessId : {ApplicationId}

     

5.  Cliquez sur **OK**.

Vous pouvez maintenant définir des points d’arrêt, démarrer le débogueur et commencer à effectuer des appels à votre composant.

## <a name="debugging-library-application-components-with-visual-c"></a>Débogage des composants d’application de la bibliothèque avec Visual C++

Pour déboguer des composants dans une application de bibliothèque, vous devez configurer le projet du client, car le processus du client hébergera l’application de bibliothèque.

**Pour activer le débogage d’application de bibliothèque avec Visual C++**

1.  Dans Visual C++, dans le menu **projet** , cliquez sur **paramètres**.

2.  Dans la boîte de dialogue **paramètres du projet** , dans la zone **paramètres pour** , cliquez sur **débogage Win32**.

3.  Sous l’onglet **Déboguer** , dans la zone **catégorie** , cliquez sur **autres dll**.

4.  Dans la liste **modules** , ajoutez les dll du composant dans votre application de bibliothèque. Cela vous permet de définir des points d’arrêt avant le chargement de votre DLL.

5.  Cliquez sur **OK**.

## <a name="debugging-without-visual-c"></a>Débogage sans Visual C++

Que vous utilisiez Visual C++ pour le débogage, vous pouvez utiliser le paramètre **lancer dans le débogueur** pour spécifier le débogueur dans lequel vos composants doivent s’exécuter.

**Pour spécifier un débogueur à partir de l’outil d’administration Services de composants**

1.  Dans l’arborescence de la console, sélectionnez l’application de bibliothèque COM+ contenant les composants que vous souhaitez déboguer.

2.  Cliquez avec le bouton droit sur l’application, puis cliquez sur **Propriétés**.

3.  Dans la boîte de dialogue **Propriétés** de l’application, cliquez sur l’onglet **avancé** .

4.  Sous **débogage**, activez la case à cocher **lancer dans le débogueur** .

5.  Dans la zone **chemin du débogueur** , entrez le chemin d’accès au débogueur que vous souhaitez utiliser. Vous pouvez également cliquer sur **Parcourir** pour rechercher le débogueur. Voici un exemple : C : \\ winnt \\ system32 \\Ntsd.exe.

6.  Cliquez sur **OK**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Débogage de composants écrits en Visual Basic](debugging-components-written-in-visual-basic.md)
</dt> </dl>

 

 



