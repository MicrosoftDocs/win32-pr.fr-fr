---
title: Certifier votre application de bureau
description: Suivez ces étapes pour obtenir votre application de bureau certifiée pour Windows 7, Windows 8, Windows 8.1 et Windows 10. Si vous souhaitez convertir votre application de bureau pour qu’elle soit compatible avec le plateforme Windows universelle et le Windows Store, vous utiliserez le pont de bureau Windows. dans ce cas, vous devez suivre les conseils sur le pont Desktop pour les étapes de certification. Si vous développez et certifiez une application UWP à partir du début, consultez conseils pour la certification des applications Windows dans UWP pour plus d’informations sur la certification.
ms.assetid: d77d9f1c-1738-4f44-a351-1985ffc21707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52eb0f1040c438cb61f4729923c8928116447e8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734557"
---
# <a name="certify-your-desktop-application"></a>Certifier votre application de bureau

> [!IMPORTANT]
> La certification pour les applications de bureau Win32 est [déconseillée](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920). À la place, [envoyez les fichiers ici](https://www.microsoft.com/wdsi/filesubmission/).

Suivez ces étapes pour obtenir votre application de bureau certifiée pour Windows 7, Windows 8, Windows 8.1 et Windows 10.

Si vous souhaitez convertir votre application de bureau pour qu’elle soit compatible avec le plateforme Windows universelle et le Windows Store, vous utiliserez le [pont de bureau Windows](https://developer.microsoft.com/windows/bridges/desktop). dans ce cas, vous devez suivre les conseils relatifs au [pont de bureau](/windows/uwp/porting/desktop-to-uwp-root) pour les étapes de certification.

Si vous développez et certifiez une application UWP à partir du début, consultez [conseils pour la certification des applications Windows dans UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) pour plus d’informations sur la certification.

## <a name="step-1-prepare-for-certification"></a>Étape 1 : préparer la certification



| Rubrique                                                                                       | Description                                                                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Quels sont les avantages ?](what-are-the-benefits-.md)<br/>                             | La certification de votre application de bureau offre plusieurs avantages à vous et à vos clients.              |
| [Lire les spécifications](certification-requirements-for-windows-desktop-apps.md)<br/> | Passez en revue les conditions techniques et les qualifications d’éligibilité qu’une application de bureau doit respecter. |



 

## <a name="step-2-test-your-app-with-the-windows-app-certification-kit"></a>Étape 2 : tester votre application avec le kit de certification des applications Windows



| Rubrique                                                          | Description                                                                                                                                                                           |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Procurez-vous le kit](https://developer.microsoft.com/windows/downloads/app-certification-kit/) | Pour certifier votre application, vous devez installer et exécuter le kit de certification des applications Windows (inclus dans le SDK Windows).                                                                     |
| [Utilisation du kit](using-the-windows-app-certification-kit.md)   | Avant de pouvoir envoyer votre application, vous devez la tester à des fins de préparation. Vous pouvez également télécharger une copie du livre [blanc](https://www.microsoft.com/download/details.aspx?id=27414)sur la certification de l’application. |
| [Examiner les détails du test](windows-app-certification-kit-tests.md) | Obtenir la liste des tests que votre application doit passer pour bénéficier d’une compatibilité avec le système d’exploitation Windows le plus récent.                                                               |



 

Remarque : les pilotes de filtre doivent également passer le [Kit de certification matérielle](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe). (Voir [conditions de certification pour les applications de bureau Windows, section 6,2](certification-requirements-for-windows-desktop-apps.md).)

## <a name="step-3-use-the-windows-certification-dashboard"></a>Étape 3 : utiliser le tableau de bord de certification Windows

Pour soumettre votre application à des fins de certification, vous devez vous connecter ou inscrire un compte d’entreprise dans le [tableau de bord de certification Windows](/previous-versions/hh833792(v=msdn.10)). Une fois que vous avez fait, non seulement vous serez en mesure d’obtenir la certification de votre application, mais vous aurez également accès à des outils pour examiner et gérer votre application à toutes les étapes du processus.



| Rubrique                                                                                                                   | Description                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configurer votre compte](/windows-hardware/drivers/dashboard/)                 | Si votre entreprise n’est pas encore inscrite, vous devez l’inscrire via le tableau de bord de certification Windows.                                        |
| [Obtenir un certificat de signature de code](/windows-hardware/drivers/dashboard/)      | Avant de pouvoir établir un compte de tableau de bord de certification Windows, vous devez obtenir un certificat de signature de code pour sécuriser vos informations numériques. |
| [Tester localement et charger les résultats](/windows-hardware/drivers/dashboard/) | Une fois que vous avez exécuté les tests du kit de certification des applications Windows, téléchargez les résultats dans le tableau de bord de certification Windows.                                 |
| [Gérer votre soumission](/windows-hardware/drivers/dashboard/)              | Une fois que vous avez envoyé votre application pour certification, vous pouvez passer en revue votre soumission via le tableau de bord de certification Windows.                           |



 

## <a name="step-4-promote-your-desktop-app"></a>Étape 4 : promouvoir votre application de bureau



| Rubrique                                                                      | Description                                                                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Vérifier la compatibilité des applications](/windows/compatibility/windows-8-1-introduction) | Si vous générez une application pour Windows 8.1, examinez les problèmes de compatibilité.                                           |
| [Utiliser le logo avec votre application](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)                  | Affichez le logo sur l’emballage, sur les publicités et d’autres documents promotionnels conformément aux instructions. Pour Windows 7 uniquement. |



 

## <a name="see-also"></a>Voir aussi :

[Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility)sur la compatibilité des applications : recherchez de l’aide auprès de la communauté sur la compatibilité et la certification du logo.

[SDK Windows blog](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): Découvrez les conseils et les actualités relatifs à la certification des applications.

[Forum Windows Server]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): visitez le Forum de certification pour obtenir des réponses.

Guide de [compatibilité](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): obtenir des informations sur les nouveautés ou les modifications apportées à la dernière version de Windows.

 

