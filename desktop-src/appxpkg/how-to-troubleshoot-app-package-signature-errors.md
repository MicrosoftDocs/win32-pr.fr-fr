---
title: Comment résoudre les erreurs de signature de package d’application
description: L’échec d’un déploiement d’application peut être dû à l’impossibilité de valider la signature numérique du package d’application. Découvrez comment reconnaître ces échecs et comment les utiliser.
ms.assetid: CE868296-87F6-4BD5-8AC5-914E429EDEBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdec41d2d058a48153d6126fea534c1efaf16e16ccabef5d5e940daa73e839a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048947"
---
# <a name="how-to-troubleshoot-app-package-signature-errors"></a>Comment résoudre les erreurs de signature de package d’application

L’échec d’un déploiement d’application peut être dû à l’impossibilité de valider la signature numérique du package d’application. Découvrez comment reconnaître ces échecs et comment les utiliser.

lorsque vous déployez une application Windows empaquetée, Windows tente toujours de valider la signature numérique sur le package d’application. Échecs lors du déploiement du bloc de validation de signature du package. Mais la raison pour laquelle le package n’a pas été validé peut ne pas être évidente. En particulier, si vous signez vos packages avec des certificats privés pour des tests locaux, vous devez souvent gérer l’approbation de ces certificats. Une configuration d’approbation de certificat incorrecte peut entraîner des échecs de validation de signature.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [empaquetage, déploiement et interrogation d’applications Windows](appx-portal.md)
-   [Vérification de l’approbation du certificat](/windows/desktop/SecCrypto/certificate-trust-verification)

### <a name="prerequisites"></a>Prérequis

-   [Windows journal des événements](/windows/desktop/WES/windows-event-log) pour diagnostiquer les échecs d’installation.
-   [Tâches certutil pour la gestion des certificats](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10)) pour la manipulation du magasin de certificats pendant le dépannage

## <a name="instructions"></a>Instructions

### <a name="step-1-examine-event-logs-for-diagnostic-information"></a>Étape 1 : examiner les journaux des événements pour obtenir des informations de diagnostic

Selon la manière dont vous avez essayé de déployer votre application, vous n’avez peut-être pas reçu de code d’erreur significatif pour l’échec du déploiement. Dans ce cas, vous pouvez généralement récupérer le code d’erreur directement à partir des journaux des événements.

**Pour récupérer le code d’erreur à partir des journaux des événements**

1.  Exécutez **eventvwr. msc**.
2.  accédez à **observateur d’événements (Local)**  >  **journaux des Applications et des Services**  >  **Microsoft**  >  **Windows**.
3.  le premier journal à vérifier est **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/operational**.
4.  les erreurs liées au déploiement sont enregistrées dans **AppXDeployment-Server**  >  **Microsoft-Windows-AppXDeploymentServer/operational**.

    Pour les erreurs de déploiement, recherchez l’événement d’erreur le plus récent 404. Cet événement d’erreur vous fournit le code d’erreur et une description de la raison de l’échec du déploiement. Si un événement d’erreur 465 a précédé l’événement 404, un problème s’est produit lors de l’ouverture du package.

si l’erreur 465 ne s’est pas produite, consultez la page [résolution des problèmes généraux, déploiement et interrogation des applications Windows](troubleshooting.md). Sinon, reportez-vous à cette table pour obtenir des codes d’erreur courants qui peuvent s’afficher dans la chaîne d’erreur pour l’événement d’erreur 465 :

| Code d'erreur | Erreur                                 | Description                                                                                                          | Suggestion                                                                                                                                                                                                 |
|------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x80073CF0 | ERREUR d’installation de l' \_ \_ ouverture du \_ package \_ | Impossible d’ouvrir le package d’application.                                                                                 | Cette erreur indique généralement un problème avec le package. Vous devez générer et signer à nouveau le package. Pour plus d’informations, consultez [utilisation d’App Packager](make-appx-package--makeappx-exe-.md). |
| 0x80080205 | APPX \_ E \_ BLOCKMAP non valide \_            | Le package d’application a été falsifié ou a un mappage de bloc non valide.                                                  | Le package est endommagé. Vous devez générer et signer à nouveau le package. Pour plus d’informations, consultez [utilisation d’App Packager](make-appx-package--makeappx-exe-.md).                                  |
| 0x800B0004 | APPROUVER \_ E \_ Subject \_ non \_ approuvé       | Le package d’application a été falsifié.                                                                              | Le contenu du package ne correspond plus à sa signature numérique. Vous devez signer à nouveau le package. Pour plus d’informations, consultez [Comment signer un package d’application à l’aide de SignTool](how-to-sign-a-package-using-signtool.md).  |
| 0x800B0100 | APPROUVER \_ E \_ NoSignature                 | Le package d’application n’est pas signé.                                                                                         | seuls les packages d’application Windows signés peuvent être déployés. Pour plus d’informations sur la signature d’un package d’application, consultez [Comment signer un package d’application à l’aide de SignTool](how-to-sign-a-package-using-signtool.md).                  |
| 0x800B0109 | CERTIFICAT \_ E \_ racine non approuvée \_              | La chaîne de certificats utilisée pour signer le package d’application se termine par un certificat racine qui n’est pas approuvé.           | Passez à l’étape 2 pour dépanner la confiance du certificat.                                                                                                                                                  |
| 0x800B010A | chaînage du certificat \_ E \_                     | Aucune chaîne de certificats n’a pu être créée à une autorité racine approuvée à partir du certificat qui a été utilisé pour signer le package d’application. | Passez à l’étape 2 pour dépanner la confiance du certificat.                                                                                                                                                  |



 

### <a name="step-2-determine-the-certificate-chain-used-to-sign-the-app-package"></a>Étape 2 : déterminer la chaîne de certificats utilisée pour signer le package d’application

Pour déterminer les certificats que l’ordinateur local doit approuver, vous pouvez examiner la chaîne de certificats pour la signature numérique sur le package d’application.

**Pour déterminer la chaîne de certificats**

1.  Dans l’Explorateur de fichiers, cliquez avec le bouton droit sur le package d’application, puis sélectionnez **Propriétés**.
2.  Dans la boîte de dialogue **Propriétés** , sélectionnez l’onglet **signatures numériques** , qui indique également si la signature peut être validée.
3.  Dans la liste signature, sélectionnez la signature, puis cliquez sur le bouton **Détails** .
4.  Dans la boîte de dialogue détails de la **signature numérique** , cliquez sur le bouton **afficher le certificat** .
5.  Dans la boîte de dialogue **certificat** , sélectionnez l’onglet **chemin d’accès de certification** .

Le certificat supérieur dans la chaîne est le certificat racine et le certificat inférieur est le certificat de signature. Si un seul certificat est présent dans la chaîne, le certificat de signature est également son propre certificat racine. Vous pouvez déterminer le numéro de série de chaque certificat que vous utilisez ensuite avec [certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)):

**Pour déterminer le numéro de série de chaque certificat**

1.  Dans le volet chemin d’accès de certification, sélectionnez le certificat, puis cliquez sur **afficher le certificat**.
2.  Dans la boîte de dialogue certificat, sélectionnez l’onglet **Détails** , qui affiche le numéro de série et d’autres propriétés utiles du certificat.

### <a name="step-3-determine-the-certificates-trusted-by-the-local-machine"></a>Étape 3 : déterminer les certificats approuvés par l’ordinateur local

Pour pouvoir déployer un package d’application, celui-ci ne doit pas être approuvé dans le contexte de l’utilisateur, mais également dans le contexte de l’ordinateur local. Par conséquent, la signature numérique peut apparaître valide quand elle est affichée sous l’onglet signatures numériques de l’étape précédente, mais qu’elle n’est toujours pas validée lors du déploiement du package d’application.

**Pour déterminer si la chaîne de certificats utilisée pour signer le package d’application est spécifiquement approuvée par l’ordinateur local**

1.  Exécutez cette commande :

    ``` syntax
    CertUtil.exe -store Root rootCertSerialNumber
    ```

2.  Exécutez cette commande :

    ``` syntax
    CertUtil.exe -store TrustedPeople signingCertSerialNumber
    ```

Si vous ne spécifiez pas le numéro de série du certificat, [certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)) répertorie tous les certificats qui sont approuvés par l’ordinateur local pour ce magasin.

L’installation du package peut échouer en raison d’erreurs de chaînage de certificats, même si le certificat de signature n’est pas auto-signé et que le certificat racine se trouve dans le magasin racine de l’ordinateur local. Dans ce cas, il peut y avoir un problème de confiance pour les autorités de certification intermédiaires. Pour plus d’informations sur ce problème, consultez [utilisation des certificats](/previous-versions/dotnet/netframework-3.0/ms731899(v=vs.85)).

## <a name="remarks"></a>Remarques

Si vous avez déterminé que le package n’a pas pu être déployé parce que le certificat de signature n’est pas approuvé, n’installez pas le package, sauf si vous connaissez son origine et que vous l’approuvez.

Si vous souhaitez approuver manuellement l’application pour l’installation (par exemple, pour installer votre propre package d’application signé par test), vous pouvez ajouter manuellement le certificat à la confiance de certificat de l’ordinateur local à partir du package d’application.

**Pour ajouter manuellement le certificat à l’approbation de certificat de l’ordinateur local**

1.  Dans l’Explorateur de fichiers, cliquez avec le bouton droit sur le package d’application, puis, dans le menu contextuel, sélectionnez **Propriétés**.
2.  Dans la boîte de dialogue **Propriétés** , sélectionnez l’onglet **signatures numériques** .
3.  Dans la liste signature, sélectionnez la signature, puis cliquez sur le bouton **Détails** .
4.  Dans la boîte de dialogue détails de la **signature numérique** , cliquez sur le bouton **afficher le certificat** .
5.  Dans la boîte de dialogue **certificat** , cliquez sur **installer le certificat...** .
6.  Dans l’Assistant importation de certificat, sélectionnez **ordinateur local** , puis cliquez sur **suivant**. Vous devez accorder des privilèges d’administrateur pour continuer.
7.  Sélectionnez **Placer tous les certificats dans le magasin suivant** et accédez au magasin de **personnes autorisées** .
8.  Cliquez sur **suivant**, puis sur **Terminer** pour terminer l’Assistant.

Après cet ajout manuel, vous pouvez voir que le certificat est maintenant approuvé dans la boîte de dialogue **certificat** .

Vous pouvez supprimer le certificat une fois que vous n’en avez plus besoin.

**Pour supprimer le certificat**

1.  Exécutez **Cmd.exe** en tant qu’administrateur.
2.  À l’invite de commandes de l’administrateur, exécutez la commande suivante :

    ``` syntax
    Certutil -store TrustedPeople
    ```

3.  Recherchez le numéro de série du certificat que vous avez installé. Ce nombre est *certID*.
4.  Exécutez cette commande :

    ``` syntax
    Certutil -delStore TrustedPeople certID
    ```

Nous vous recommandons d’éviter d’ajouter manuellement des certificats racines au [magasin de certificats des autorités de certification racines de confiance](/windows-hardware/drivers/install/trusted-root-certification-authorities-certificate-store)de l’ordinateur local. Il peut être plus efficace d’avoir plusieurs applications signées avec des certificats qui s’enchaînent au même certificat racine, comme des applications métier, que d’installer des certificats individuels dans le magasin de personnes autorisées. Le magasin de personnes autorisées contient des certificats considérés comme approuvés par défaut. par conséquent, ils ne sont pas vérifiés par des autorités plus ou des listes de certificats de confiance. Pour plus d’informations sur l’ajout de certificats au magasin de certificats des autorités de certification racines de confiance, consultez [meilleures pratiques](/previous-versions/windows/hardware/design/dn653556(v=vs.85))pour la signature de code.

## <a name="security-considerations"></a>Considérations relatives à la sécurité

En ajoutant un certificat aux [magasins de certificats de l’ordinateur local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), vous affectez le certificat de confiance de tous les utilisateurs sur l’ordinateur. Nous vous recommandons d’installer les certificats de signature de code que vous souhaitez pour tester des packages d’application dans le magasin de certificats personnes autorisées. Supprimez rapidement ces certificats lorsqu’ils ne sont plus nécessaires pour les empêcher d’être utilisés pour compromettre la confiance du système. Si vous créez vos propres certificats de test pour la signature des packages d’application, nous vous recommandons également de limiter les privilèges associés au certificat de test. Pour plus d’informations sur la création de certificats de test pour la signature de packages d’application, consultez [comment créer un certificat de signature de package d’application](how-to-create-a-package-signing-certificate.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Exemples**
</dt> <dt>

[Exemple de création de package d’application](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Concepts**
</dt> <dt>

[Résolution des problèmes d’empaquetage, de déploiement et d’interrogation des applications Windows](troubleshooting.md)
</dt> <dt>

[Tâches certutil pour la gestion des certificats](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10))
</dt> </dl>

 

 
